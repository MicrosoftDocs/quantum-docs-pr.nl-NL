---
title: Kwantumsimulatoren en hosttoepassingen | Microsoft Docs
description: Hierin wordt beschreven hoe u kwantumsimulatoren kunt aansturen met een klassieke .NET-programmeertaal, zoals C# of Q#.
author: QuantumWriter
ms.author: Alan.Geller@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines
ms.openlocfilehash: 14aed75ed0ed192f88699b1c7dbacfae23f74642
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85273335"
---
# <a name="quantum-simulators-and-host-applications"></a><span data-ttu-id="743f4-103">Kwantumsimulatoren en hosttoepassingen</span><span class="sxs-lookup"><span data-stu-id="743f4-103">Quantum simulators and host applications</span></span>

## <a name="what-youll-learn"></a><span data-ttu-id="743f4-104">U leert het volgende</span><span class="sxs-lookup"><span data-stu-id="743f4-104">What You'll Learn</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="743f4-105">Hoe kwantumalgoritmen worden uitgevoerd</span><span class="sxs-lookup"><span data-stu-id="743f4-105">How quantum algorithms are executed</span></span>
> * <span data-ttu-id="743f4-106">Welke kwantumsimulatoren deze versie bevat</span><span class="sxs-lookup"><span data-stu-id="743f4-106">What quantum simulators are included in this release</span></span>
> * <span data-ttu-id="743f4-107">Hoe u een C#-stuurprogramma schrijft voor uw kwantumalgoritme</span><span class="sxs-lookup"><span data-stu-id="743f4-107">How to write a C# driver for your quantum algorithm</span></span>

## <a name="the-quantum-development-kit-execution-model"></a><span data-ttu-id="743f4-108">Het uitvoeringsmodel van de Quantum development kit</span><span class="sxs-lookup"><span data-stu-id="743f4-108">The Quantum Development Kit Execution Model</span></span>

<span data-ttu-id="743f4-109">In [Een kwantumprogramma schrijven](xref:microsoft.quantum.write-program) hebben we ons kwantumalgoritme uitgevoerd door het object `QuantumSimulator` door te geven aan de methode `Run` van de algoritmeklasse.</span><span class="sxs-lookup"><span data-stu-id="743f4-109">In [Writing a quantum program](xref:microsoft.quantum.write-program), we executed our quantum algorithm by passing a `QuantumSimulator` object to the algorithm class's `Run` method.</span></span>
<span data-ttu-id="743f4-110">De klasse `QuantumSimulator` voert het kwantumalgoritme uit door de kwantumtoestandsvector volledig te simuleren, wat perfect is voor het uitvoeren en testen van `Teleport`.</span><span class="sxs-lookup"><span data-stu-id="743f4-110">The `QuantumSimulator` class executes the quantum algorithm by fully simulating the quantum state vector, which is perfect for running and testing `Teleport`.</span></span>
<span data-ttu-id="743f4-111">Zie de [handleiding Concepten](xref:microsoft.quantum.concepts.intro) voor meer informatie over kwantumtoestandsvectoren.</span><span class="sxs-lookup"><span data-stu-id="743f4-111">See the [Concepts guide](xref:microsoft.quantum.concepts.intro) for more on quantum state vectors.</span></span>

<span data-ttu-id="743f4-112">Andere doelcomputers kunnen worden gebruikt om een kwantumalgoritme uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="743f4-112">Other target machines may be used to run a quantum algorithm.</span></span>
<span data-ttu-id="743f4-113">De computer is verantwoordelijk voor het leveren van de implementaties van kwantumprimitieven voor het algoritme.</span><span class="sxs-lookup"><span data-stu-id="743f4-113">The machine is responsible for providing implementations of quantum primitives for the algorithm.</span></span>
<span data-ttu-id="743f4-114">Dit omvat primitieve bewerkingen, zoals H, CNOT en Measure, plus qubitbeheer en -tracering.</span><span class="sxs-lookup"><span data-stu-id="743f4-114">This includes primitive operations such as H, CNOT, and Measure, as well as qubit management and tracking.</span></span>
<span data-ttu-id="743f4-115">Verschillende klassen van kwantumcomputers vertegenwoordigen verschillende uitvoeringsmodellen voor hetzelfde kwantumalgoritme.</span><span class="sxs-lookup"><span data-stu-id="743f4-115">Different classes of quantum machines represent different execution models for the same quantum algorithm.</span></span>

<span data-ttu-id="743f4-116">Op elk type kwantumcomputer kunnen verschillende implementaties van deze primitieven worden geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="743f4-116">Each type of quantum machine may provide different implementations of these primitives.</span></span>
<span data-ttu-id="743f4-117">Met de kwantumcomputer-traceersimulator die deel uitmaakt van de development kit wordt bijvoorbeeld helemaal geen simulatie uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="743f4-117">For instance, the quantum computer trace simulator included in the development kit doesn't do any simulation at all.</span></span>
<span data-ttu-id="743f4-118">In plaats daarvan worden het gebruik van gates, qubits en andere resources bijgehouden voor het algoritme.</span><span class="sxs-lookup"><span data-stu-id="743f4-118">Rather, it tracks gate, qubit, and other resource usage for the algorithm.</span></span>

### <a name="quantum-machines"></a><span data-ttu-id="743f4-119">Kwantumcomputers</span><span class="sxs-lookup"><span data-stu-id="743f4-119">Quantum Machines</span></span>

<span data-ttu-id="743f4-120">In de toekomst zullen we aanvullende kwantumcomputerklassen definiëren om andere typen simulaties en uitvoering op topologische kwantumcomputers te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="743f4-120">In the future, we will define additional quantum machine classes to support other types of simulation and to support execution on topological quantum computers.</span></span>
<span data-ttu-id="743f4-121">Het algoritme kan constant blijven terwijl de onderliggende computerimplementatie wordt gewijzigd. Dit maakt het eenvoudig om een algoritme in simulatie te testen en fouten op te sporen en het vervolgens op echte hardware uit te voeren in de wetenschap dat het algoritme niet is gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="743f4-121">Allowing the algorithm to stay constant while varying the underlying machine implementation makes it easy to test and debug an algorithm in simulation and then run it on real hardware with confidence that the algorithm hasn't changed.</span></span>

### <a name="whats-included-in-this-release"></a><span data-ttu-id="743f4-122">Wat bevat deze versie?</span><span class="sxs-lookup"><span data-stu-id="743f4-122">What's Included in this Release</span></span>

<span data-ttu-id="743f4-123">Deze versie van de Quantum Development Kit bevat verschillende kwantumcomputerklassen.</span><span class="sxs-lookup"><span data-stu-id="743f4-123">This release of the quantum developer kit includes several quantum machine classes.</span></span>
<span data-ttu-id="743f4-124">Deze zijn allemaal gedefinieerd in de naamruimte `Microsoft.Quantum.Simulation.Simulators`.</span><span class="sxs-lookup"><span data-stu-id="743f4-124">All of them are defined in the `Microsoft.Quantum.Simulation.Simulators` namespace.</span></span>

* <span data-ttu-id="743f4-125">Een [volledige toestandsvectorsimulator](xref:microsoft.quantum.machines.full-state-simulator), de klasse `QuantumSimulator`.</span><span class="sxs-lookup"><span data-stu-id="743f4-125">A [full state vector simulator](xref:microsoft.quantum.machines.full-state-simulator), the `QuantumSimulator` class.</span></span>
* <span data-ttu-id="743f4-126">Een [eenvoudige resource-estimator](xref:microsoft.quantum.machines.resources-estimator), de klasse `ResourcesEstimator`, waarmee u een algemene schatting kunt maken van de benodigde resources voor het uitvoeren van een kwantumalgoritme.</span><span class="sxs-lookup"><span data-stu-id="743f4-126">A [simple resources estimator](xref:microsoft.quantum.machines.resources-estimator), the `ResourcesEstimator` class, it allows a top level analysis of the resources needed to run a quantum algorithm.</span></span>
* <span data-ttu-id="743f4-127">Een [op tracering gebaseerde resource-estimator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), de klasse `QCTraceSimulator`, waarmee u een geavanceerde analyse kunt maken van de verbruikte resources voor de hele call-graph (aanroepgrafiek) van het algoritme.</span><span class="sxs-lookup"><span data-stu-id="743f4-127">A [trace-based resource estimator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), the `QCTraceSimulator` class, it allows advanced analysis of resources consumptions for the algorithm's entire call-graph.</span></span>
* <span data-ttu-id="743f4-128">Een [Toffoli-simulator](xref:microsoft.quantum.machines.toffoli-simulator), de klasse `ToffoliSimulator`.</span><span class="sxs-lookup"><span data-stu-id="743f4-128">A [Toffoli simulator](xref:microsoft.quantum.machines.toffoli-simulator), the `ToffoliSimulator` class.</span></span>

## <a name="writing-a-host-application"></a><span data-ttu-id="743f4-129">Een hosttoepassing schrijven</span><span class="sxs-lookup"><span data-stu-id="743f4-129">Writing a host application</span></span>

<span data-ttu-id="743f4-130">In [Een kwantumprogramma schrijven](xref:microsoft.quantum.write-program) hebben we een eenvoudig C#-stuurprogramma voor ons teleporteeralgoritme geschreven.</span><span class="sxs-lookup"><span data-stu-id="743f4-130">In [Writing a quantum program](xref:microsoft.quantum.write-program), we wrote a simple C# driver for our teleport algorithm.</span></span> <span data-ttu-id="743f4-131">Een C#-stuurprogramma heeft 4 hoofddoelen:</span><span class="sxs-lookup"><span data-stu-id="743f4-131">A C# driver has 4 main purposes:</span></span>

* <span data-ttu-id="743f4-132">De doelcomputer maken</span><span class="sxs-lookup"><span data-stu-id="743f4-132">Constructing the target machine</span></span>
* <span data-ttu-id="743f4-133">Eventuele benodigde argumenten voor het kwantumalgoritme berekenen</span><span class="sxs-lookup"><span data-stu-id="743f4-133">Computing any arguments required for the quantum algorithm</span></span>
* <span data-ttu-id="743f4-134">Het kwantumalgoritme uitvoeren met behulp van de simulator</span><span class="sxs-lookup"><span data-stu-id="743f4-134">Running the quantum algorithm using the simulator</span></span>
* <span data-ttu-id="743f4-135">Het resultaat van de bewerking verwerken</span><span class="sxs-lookup"><span data-stu-id="743f4-135">Processing the result of the operation</span></span>

<span data-ttu-id="743f4-136">Hieronder bespreken we elke stap in meer detail.</span><span class="sxs-lookup"><span data-stu-id="743f4-136">Here we'll discuss each step in more detail.</span></span>

### <a name="constructing-the-target-machine"></a><span data-ttu-id="743f4-137">De doelcomputer maken</span><span class="sxs-lookup"><span data-stu-id="743f4-137">Constructing the Target Machine</span></span>

<span data-ttu-id="743f4-138">Kwantumcomputers zijn exemplaren van normale .NET-klassen en worden, net als elke andere .NET-klasse, gemaakt door hun constructor aan te roepen.</span><span class="sxs-lookup"><span data-stu-id="743f4-138">Quantum machines are instances of normal .NET classes, so they are created by invoking their constructor, just like any .NET class.</span></span>
<span data-ttu-id="743f4-139">Sommige simulatoren, met inbegrip van de `QuantumSimulator`, implementeren de .NET-interface <xref:System.IDisposable?displayProperty=nameWithType> en moeten dus worden verpakt in een C#-instructie met `using`.</span><span class="sxs-lookup"><span data-stu-id="743f4-139">Some simulators, including the `QuantumSimulator`, implement the .NET <xref:System.IDisposable?displayProperty=nameWithType> interface, and so should be wrapped in a C# `using` statement.</span></span>

### <a name="computing-arguments-for-the-algorithm"></a><span data-ttu-id="743f4-140">Argumenten berekenen voor het algoritme</span><span class="sxs-lookup"><span data-stu-id="743f4-140">Computing Arguments for the Algorithm</span></span>

<span data-ttu-id="743f4-141">In het voorbeeld `Teleport` hebben we enkele relatief kunstmatige argumenten berekend om die door te geven aan het kwantumalgoritme.</span><span class="sxs-lookup"><span data-stu-id="743f4-141">In our `Teleport` example, we computed some relatively artificial arguments to pass to our quantum algorithm.</span></span>
<span data-ttu-id="743f4-142">Doorgaans is er een aanzienlijke hoeveelheid gegevens nodig voor het kwantumalgoritme. Het is het gemakkelijkst om deze op te geven via het klassieke stuurprogramma.</span><span class="sxs-lookup"><span data-stu-id="743f4-142">More typically, however, there is significant data required by the quantum algorithm, and it is easiest to provide it from the classical driver.</span></span>

<span data-ttu-id="743f4-143">Bij het uitvoeren van chemische simulaties is voor het kwantumalgoritme bijvoorbeeld een grote tabel met moleculaire orbitaalinteractie-integralen vereist.</span><span class="sxs-lookup"><span data-stu-id="743f4-143">For instance, when doing chemical simulations, the quantum algorithm requires a large table of molecular orbital interaction integrals.</span></span>
<span data-ttu-id="743f4-144">Over het algemeen worden deze gelezen vanuit een bestand dat wordt aangeleverd bij het uitvoeren van het algoritme.</span><span class="sxs-lookup"><span data-stu-id="743f4-144">Generally these are read in from a file that is provided when running the algorithm.</span></span>
<span data-ttu-id="743f4-145">Omdat in Q# geen mechanisme bestaat voor het openen van het bestandssysteem, kunnen dergelijke gegevens het beste worden verzameld via het klassieke stuurprogramma en vervolgens worden doorgegeven aan de methode `Run` van het kwantumalgoritme.</span><span class="sxs-lookup"><span data-stu-id="743f4-145">Since Q# does not have a mechanism for accessing the file system, this sort of data is best collected by the classical driver and then passed to the quantum algorithm's `Run` method.</span></span>

<span data-ttu-id="743f4-146">Ook bij variabele methoden speelt het klassieke stuurprogramma een belangrijke rol.</span><span class="sxs-lookup"><span data-stu-id="743f4-146">Another case where the classical driver plays a key role is in variational methods.</span></span>
<span data-ttu-id="743f4-147">In deze klasse van algoritmen wordt een kwantumtoestand voorbereid op basis van enkele klassieke parameters, en wordt die toestand gebruikt voor het berekenen van een bepaalde waarde.</span><span class="sxs-lookup"><span data-stu-id="743f4-147">In this class of algorithms, a quantum state is prepared based on some classical parameters, and that state is used to compute some value of interest.</span></span>
<span data-ttu-id="743f4-148">De parameters worden aangepast op basis van een type Hill Climbing- of machine learning-algoritme en het kwantumalgoritme wordt opnieuw uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="743f4-148">The parameters are adjusted based on some type of hill climbing or machine learning algorithm and the quantum algorithm run again.</span></span>
<span data-ttu-id="743f4-149">Voor dergelijke algoritmen kan het Hill Climbing-algoritme zelf het beste worden geïmplementeerd als een louter klassieke functie die wordt aangeroepen door het klassieke stuurprogramma; de resultaten van het Hill Climbing-algoritme worden vervolgens doorgegeven aan de volgende uitvoering van het kwantumalgoritme.</span><span class="sxs-lookup"><span data-stu-id="743f4-149">For such algorithms, the hill climbing algorithm itself is best implemented as a purely classical function that is called by the classical driver; the results of the hill climbing are then passed to the next execution of the quantum algorithm.</span></span>

### <a name="running-the-quantum-algorithm"></a><span data-ttu-id="743f4-150">Het kwantumalgoritme uitvoeren</span><span class="sxs-lookup"><span data-stu-id="743f4-150">Running the Quantum Algorithm</span></span>

<span data-ttu-id="743f4-151">Dit deel is over het algemeen zeer eenvoudig.</span><span class="sxs-lookup"><span data-stu-id="743f4-151">This part is generally very straightforward.</span></span>
<span data-ttu-id="743f4-152">Elke Q#-bewerking wordt gecompileerd in een klasse die voorziet in een statische `Run`-methode.</span><span class="sxs-lookup"><span data-stu-id="743f4-152">Each Q# operation is compiled into a class that provides a static `Run` method.</span></span>
<span data-ttu-id="743f4-153">De argumenten voor deze methode worden doorgegeven door de tuple van het afgevlakte argument van de bewerking zelf, plus een extra eerste argument voor de simulator waarmee de methode moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="743f4-153">The arguments to this method are given by the flattened argument tuple of the operation itself, plus an additional first argument which is the simulator to execute with.</span></span> <span data-ttu-id="743f4-154">Voor een bewerking waarin de benoemde tuple van het type `(a: String, (b: Double, c: Double))` wordt verwacht, is het afgevlakte equivalent van het type `(String a, Double b, Double c)`.</span><span class="sxs-lookup"><span data-stu-id="743f4-154">For an operation that expects the named tuple of type `(a: String, (b: Double, c: Double))` its flattened counterpart is of type `(String a, Double b, Double c)`.</span></span>


<span data-ttu-id="743f4-155">Er zijn wel enkele subtiliteiten om rekening mee te houden bij het doorgeven van argumenten aan een `Run`-methode:</span><span class="sxs-lookup"><span data-stu-id="743f4-155">There are some subtleties when passing arguments to a `Run` method:</span></span>

* <span data-ttu-id="743f4-156">Matrices moeten worden verpakt in een `Microsoft.Quantum.Simulation.Core.QArray<T>`-object.</span><span class="sxs-lookup"><span data-stu-id="743f4-156">Arrays must be wrapped in a `Microsoft.Quantum.Simulation.Core.QArray<T>` object.</span></span>
    <span data-ttu-id="743f4-157">Een `QArray`-klasse heeft een constructor waarin u een geordende verzameling (`IEnumerable<T>`) van de juiste objecten kunt opgeven.</span><span class="sxs-lookup"><span data-stu-id="743f4-157">A `QArray` class has a constructor that can take any ordered collection (`IEnumerable<T>`) of appropriate objects.</span></span>
* <span data-ttu-id="743f4-158">De lege tuple, `()` in Q#, wordt opgegeven met `QVoid.Instance` in C#.</span><span class="sxs-lookup"><span data-stu-id="743f4-158">The empty tuple, `()` in Q#, is represented by `QVoid.Instance` in C#.</span></span>
* <span data-ttu-id="743f4-159">Niet-lege tuples worden opgegeven als .NET `ValueTuple`-exemplaren.</span><span class="sxs-lookup"><span data-stu-id="743f4-159">Non-empty tuples are represented as .NET `ValueTuple` instances.</span></span>
* <span data-ttu-id="743f4-160">Door de gebruiker gedefinieerde typen in Q# worden doorgegeven als het bijbehorende basistype.</span><span class="sxs-lookup"><span data-stu-id="743f4-160">Q# user-defined types are passed as their base type.</span></span>
* <span data-ttu-id="743f4-161">Als u een bewerking of functie wilt doorgeven aan een `Run`-methode, moet u een exemplaar van de klasse van de bewerking of functie verkrijgen met behulp van de methode `Get<>` van de simulator.</span><span class="sxs-lookup"><span data-stu-id="743f4-161">To pass an operation or a function to a `Run` method, you have to obtain an   instance of the operation's or function's class, using the simulator's `Get<>` method.</span></span>

### <a name="processing-the-results"></a><span data-ttu-id="743f4-162">De resultaten verwerken</span><span class="sxs-lookup"><span data-stu-id="743f4-162">Processing the Results</span></span>

<span data-ttu-id="743f4-163">De resultaten van het kwantumalgoritme worden geretourneerd met behulp van de methode `Run`.</span><span class="sxs-lookup"><span data-stu-id="743f4-163">The results of the quantum algorithm are returned from the `Run` method.</span></span>
<span data-ttu-id="743f4-164">De methode `Run` wordt asynchroon uitgevoerd zodat er een exemplaar van <xref:System.Threading.Tasks.Task`1> wordt geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="743f4-164">The `Run` method executes asynchronously thus it returns an instance of <xref:System.Threading.Tasks.Task`1>.</span></span>
<span data-ttu-id="743f4-165">Er zijn meerdere manieren om de werkelijke resultaten van de bewerking te verkrijgen.</span><span class="sxs-lookup"><span data-stu-id="743f4-165">There are multiple ways to get the actual operation's results.</span></span> <span data-ttu-id="743f4-166">De eenvoudigste manier is met behulp van de eigenschap [`Result` van `Task`](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task-1.result):</span><span class="sxs-lookup"><span data-stu-id="743f4-166">The simplest is by using the `Task`'s [`Result` property](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task-1.result):</span></span>

```csharp
    var res = BellTest.Run(sim, 1000, initial).Result;
```
<span data-ttu-id="743f4-167">maar andere technieken, zoals het gebruik van de methode [`Wait`](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task.wait) of het C#-sleutelwoord [`await`](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/await) werken ook.</span><span class="sxs-lookup"><span data-stu-id="743f4-167">but other techniques, like using the [`Wait` method](https://docs.microsoft.com/dotnet/api/system.threading.tasks.task.wait) or C# [`await` keyword](https://docs.microsoft.com/dotnet/csharp/language-reference/keywords/await) will also work.</span></span>

<span data-ttu-id="743f4-168">Net als bij argumenten, worden Q#-tuples weergegeven als exemplaren van `ValueTuple`, en Q#-matrices als exemplaren van `QArray`.</span><span class="sxs-lookup"><span data-stu-id="743f4-168">As with arguments, Q# tuples are represented as `ValueTuple` instances and Q# arrays are represented as `QArray` instances.</span></span>
<span data-ttu-id="743f4-169">Door de gebruiker gedefinieerde typen worden geretourneerd als de bijbehorende basistypen.</span><span class="sxs-lookup"><span data-stu-id="743f4-169">User-defined types are returned as their base types.</span></span>
<span data-ttu-id="743f4-170">De lege tuple, `()`, wordt geretourneerd als een exemplaar van de klasse `QVoid`.</span><span class="sxs-lookup"><span data-stu-id="743f4-170">The empty tuple, `()`, is returned as an instance of the `QVoid` class.</span></span>

<span data-ttu-id="743f4-171">Voor veel kwantumalgoritmen is een aanzienlijke hoeveelheid naverwerking nodig om nuttige antwoorden te kunnen afleiden.</span><span class="sxs-lookup"><span data-stu-id="743f4-171">Many quantum algorithms require substantial post-processing to derive useful answers.</span></span>
<span data-ttu-id="743f4-172">Het kwantumdeel van het algoritme van Shor is slechts het begin van een berekening waarmee de factoren van een getal worden gevonden.</span><span class="sxs-lookup"><span data-stu-id="743f4-172">For instance, the quantum part of Shor's algorithm is just the beginning of a computation that finds the factors of a number.</span></span>

<span data-ttu-id="743f4-173">In de meeste gevallen kan dergelijke naverwerking het snelst en eenvoudigst worden uitgevoerd in het klassieke stuurprogramma.</span><span class="sxs-lookup"><span data-stu-id="743f4-173">In most cases, it is simplest and easiest to do this sort of post-processing in the classical driver.</span></span>
<span data-ttu-id="743f4-174">Alleen met het klassieke stuurprogramma kunnen resultaten worden gerapporteerd aan de gebruiker of naar schijf worden geschreven.</span><span class="sxs-lookup"><span data-stu-id="743f4-174">Only the classical driver can report results to the user or write them to disk.</span></span>
<span data-ttu-id="743f4-175">Het klassieke stuurprogramma biedt toegang tot analysebibliotheken en andere wiskundige functies die niet beschikbaar zijn in Q#.</span><span class="sxs-lookup"><span data-stu-id="743f4-175">The classical driver will have access to analytical libraries and other mathematical functions that are not exposed in Q#.</span></span>


## <a name="failures"></a><span data-ttu-id="743f4-176">Fouten</span><span class="sxs-lookup"><span data-stu-id="743f4-176">Failures</span></span>

<span data-ttu-id="743f4-177">Wanneer de Q#-instructie `fail` wordt bereikt tijdens het uitvoeren van een bewerking, wordt er een `ExecutionFailException`-uitzondering gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="743f4-177">When the Q# `fail` statement is reached during the execution of an operation, an `ExecutionFailException` is thrown.</span></span>

<span data-ttu-id="743f4-178">Als gevolg van het gebruik van `System.Task` in de methode `Run`, wordt de uitzondering die is opgetreden als gevolg van een `fail`-instructie verpakt in een `System.AggregateException`.</span><span class="sxs-lookup"><span data-stu-id="743f4-178">Due to the use of `System.Task` in the `Run` method, the exception thrown as a result of a `fail` statement will be wrapped into a `System.AggregateException`.</span></span>
<span data-ttu-id="743f4-179">Als u de werkelijke oorzaak van de fout wilt achterhalen, moet u dit herhalen in de `AggregateException` 
`InnerExceptions`, bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="743f4-179">To find the actual reason for the failure, you need to iterate into the `AggregateException` 
`InnerExceptions`, for example:</span></span>

```csharp

            try
            {
                using(var sim = new QuantumSimulator())
                {
                    /// call your operations here...
                }
            }
            catch (AggregateException e)
            {
                // Unwrap AggregateException to get the message from Q# fail statement.
                // Go through all inner exceptions.
                foreach (Exception inner in e.InnerExceptions)
                {
                    // If the exception of type ExecutionFailException
                    if (inner is ExecutionFailException failException)
                    {
                        // Print the message it contains
                        Console.WriteLine($" {failException.Message}");
                    }
                }
            }
```

## <a name="other-classical-languages"></a><span data-ttu-id="743f4-180">Andere klassieke talen</span><span class="sxs-lookup"><span data-stu-id="743f4-180">Other Classical Languages</span></span>

<span data-ttu-id="743f4-181">Hoewel de gegeven voorbeelden zijn geschreven in C#, F# en Python, biedt de Quantum development kit ook ondersteuning voor het schrijven van klassieke hostprogramma's in andere talen.</span><span class="sxs-lookup"><span data-stu-id="743f4-181">While the samples we have provided are in C#, F#, and Python, the Quantum Development Kit also supports writing classical host programs in other languages.</span></span>
<span data-ttu-id="743f4-182">Als u bijvoorbeeld een hostprogramma wilt schrijven in Visual Basic, [zou het programma gewoon moeten werken](https://github.com/tcNickolas/MiscQSharp/blob/master/Quantum_VBNet/README.md#using-q-with-visual-basic-net).</span><span class="sxs-lookup"><span data-stu-id="743f4-182">For example, if you want to write a host program in Visual Basic, [it should work just fine](https://github.com/tcNickolas/MiscQSharp/blob/master/Quantum_VBNet/README.md#using-q-with-visual-basic-net).</span></span>