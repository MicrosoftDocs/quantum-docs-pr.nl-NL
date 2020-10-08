---
title: 'Kwantumtraceersimulator: Quantum Development Kit'
description: Meer informatie over hoe u de Microsoft-kwantumcomputertraceersimulator kunt gebruiken om fouten in klassieke code op te sporen en om resourcevereisten van een Q#-programma in te schatten.
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
no-loc:
- Q#
- $$v
ms.openlocfilehash: 7f5e25aa7b58277642783e03d03854cd75ff4ca3
ms.sourcegitcommit: d98190988ff03146d9ca2b0d325870cd717d729a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/06/2020
ms.locfileid: "91771292"
---
# <a name="microsoft-quantum-development-kit-qdk-quantum-trace-simulator"></a><span data-ttu-id="152ce-103">Microsoft Quantum Development Kit (QDK)-kwantumtraceersimulator</span><span class="sxs-lookup"><span data-stu-id="152ce-103">Microsoft Quantum Development Kit (QDK) quantum trace simulator</span></span>

<span data-ttu-id="152ce-104">De QDK-klasse <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> voert een kwantumprogramma uit zonder de status van een kwantumcomputer werkelijk te simuleren.</span><span class="sxs-lookup"><span data-stu-id="152ce-104">The QDK <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> class runs a quantum program without actually simulating the state of a quantum computer.</span></span> <span data-ttu-id="152ce-105">Daarom kunnen met de kwantumtraceersimulator kwantumprogramma's van duizenden qubits worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="152ce-105">For this reason, the quantum trace simulator is able to run quantum programs that use thousands of qubits.</span></span>  <span data-ttu-id="152ce-106">De simulator is handig voor twee hoofddoelen:</span><span class="sxs-lookup"><span data-stu-id="152ce-106">It is useful for two main purposes:</span></span> 

* <span data-ttu-id="152ce-107">Het opsporen van fouten in klassieke code die deel uitmaakt van een kwantumprogramma.</span><span class="sxs-lookup"><span data-stu-id="152ce-107">Debugging classical code that is part of a quantum program.</span></span> 
* <span data-ttu-id="152ce-108">Het schatten van de benodigde resources voor het uitvoeren van een bepaald exemplaar van een kwantumprogramma op een kwantumcomputer.</span><span class="sxs-lookup"><span data-stu-id="152ce-108">Estimating the resources required to run a given instance of a quantum program on a quantum computer.</span></span> <span data-ttu-id="152ce-109">De [Resources-estimator](xref:microsoft.quantum.machines.resources-estimator), waarmee een beperkt aantal metrische gegevens wordt geboden, is gebaseerd op de traceersimulator.</span><span class="sxs-lookup"><span data-stu-id="152ce-109">In fact, the [Resources estimator](xref:microsoft.quantum.machines.resources-estimator), which provides a more limited set of metrics, is built upon the trace simulator.</span></span>

## <a name="invoking-the-quantum-trace-simulator"></a><span data-ttu-id="152ce-110">De kwantumtraceersimulator aanroepen</span><span class="sxs-lookup"><span data-stu-id="152ce-110">Invoking the quantum trace simulator</span></span>

<span data-ttu-id="152ce-111">U kunt de kwantumtraceersimulator gebruiken om een Q#-bewerking uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="152ce-111">You can use the quantum trace simulator to run any Q# operation.</span></span>

<span data-ttu-id="152ce-112">Net als bij andere doelmachines maakt u eerst een exemplaar van de klasse `QCTraceSimulator` en geeft u deze vervolgens door als de eerste parameter van de methode `Run` van een bewerking.</span><span class="sxs-lookup"><span data-stu-id="152ce-112">As with other target machines, you first create an instance of the `QCTraceSimulator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="152ce-113">Houd er rekening mee dat, in tegenstelling tot de klasse `QuantumSimulator`, de klasse `QCTraceSimulator` de interface <xref:System.IDisposable> niet implementeert, zodat u deze niet hoeft in te sluiten in een instructie `using`.</span><span class="sxs-lookup"><span data-stu-id="152ce-113">Note that, unlike the `QuantumSimulator` class, the `QCTraceSimulator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            QCTraceSimulator sim = new QCTraceSimulator();
            var res = MyQuantumProgram.Run(sim).Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="152ce-114">De waarschijnlijkheid van metingsresultaten opgeven</span><span class="sxs-lookup"><span data-stu-id="152ce-114">Providing the probability of measurement outcomes</span></span>

<span data-ttu-id="152ce-115">Omdat de kwantumtraceersimulator de werkelijke kwantumstatus niet simuleert, kan de kans op het meten van resultaten binnen een bewerking niet worden berekend.</span><span class="sxs-lookup"><span data-stu-id="152ce-115">Because the quantum trace simulator does not simulate the actual quantum state, it cannot calculate the probability of measurement outcomes within an operation.</span></span> 

<span data-ttu-id="152ce-116">Als een bewerking metingen bevat, moet u deze kansen daarom expliciet opgeven met behulp van de bewerking <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> uit de naamruimte <xref:microsoft.quantum.diagnostics>.</span><span class="sxs-lookup"><span data-stu-id="152ce-116">Therefore, if an operation includes measurements, you must explicitly provide these probabilities using the <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> operation from the <xref:microsoft.quantum.diagnostics> namespace.</span></span> <span data-ttu-id="152ce-117">Het volgende voorbeeld illustreert dit:</span><span class="sxs-lookup"><span data-stu-id="152ce-117">The following example illustrates this:</span></span>

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertMeasurementProbability([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertMeasurementProbability([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

<span data-ttu-id="152ce-118">Wanneer de kwantumtraceersimulator de `AssertMeasurementProbability` tegenkomt, wordt vastgelegd dat aan meting `PauliZ` op `source` en `q` een resultaat van `Zero` met een waarschijnlijkheid van **0,5** moet worden toegekend.</span><span class="sxs-lookup"><span data-stu-id="152ce-118">When the quantum trace simulator encounters `AssertMeasurementProbability` it records that measuring `PauliZ` on `source` and `q` should give an outcome of `Zero`, with probability **0.5**.</span></span> <span data-ttu-id="152ce-119">Wanneer de bewerking `M` later wordt uitgevoerd, worden de vastgelegde waarden van de resultaatkansen gevonden en retourneert `M` `Zero` of `One`, met een waarschijnlijkheid van **0,5**.</span><span class="sxs-lookup"><span data-stu-id="152ce-119">When it runs the `M` operation later, it finds the recorded values of the outcome probabilities, and `M` returns `Zero` or `One`, with probability **0.5**.</span></span> <span data-ttu-id="152ce-120">Wanneer dezelfde code wordt uitgevoerd in een simulator die de kwantumtoestand bijhoudt, wordt in die simulator gecontroleerd of de in `AssertMeasurementProbability` opgegeven waarschijnlijkheden juist zijn.</span><span class="sxs-lookup"><span data-stu-id="152ce-120">When the same code runs on a simulator that keeps track of the quantum state, that simulator checks that the provided probabilities in `AssertMeasurementProbability` are correct.</span></span>

<span data-ttu-id="152ce-121">Als een of meer meetbewerkingen niet zijn geannoteerd met behulp van `AssertMeasurementProbability`, wordt door de simulator een [`UnconstrainedMeasurementException`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.unconstrainedmeasurementexception) geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="152ce-121">Note that if there is at least one measurement operation that is not annotated using `AssertMeasurementProbability`, the simulator throws an [`UnconstrainedMeasurementException`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.unconstrainedmeasurementexception).</span></span>

## <a name="quantum-trace-simulator-tools"></a><span data-ttu-id="152ce-122">Hulpprogramma's voor de kwantumtraceersimulator</span><span class="sxs-lookup"><span data-stu-id="152ce-122">Quantum trace simulator tools</span></span>

<span data-ttu-id="152ce-123">De QDK bevat vijf hulpprogramma's die u met de kwantumtraceersimulator kunt gebruiken om fouten in uw programma's op te sporen en de resourceschattingen van het kwantumprogramma uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="152ce-123">The QDK includes five tools that you can use with the quantum trace simulator to detect bugs in your programs and perform quantum program resource estimates:</span></span> 

|<span data-ttu-id="152ce-124">Hulpprogramma</span><span class="sxs-lookup"><span data-stu-id="152ce-124">Tool</span></span> | <span data-ttu-id="152ce-125">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="152ce-125">Description</span></span> |
|-----| -----|
|[<span data-ttu-id="152ce-126">Controle op verschillende invoer</span><span class="sxs-lookup"><span data-stu-id="152ce-126">Distinct inputs checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) |<span data-ttu-id="152ce-127">Controleert op mogelijke conflicten met gedeelde qubits</span><span class="sxs-lookup"><span data-stu-id="152ce-127">Checks for potential conflicts with shared qubits</span></span> |
|[<span data-ttu-id="152ce-128">Controle op het gebruik van ongeldige qubits</span><span class="sxs-lookup"><span data-stu-id="152ce-128">Invalidated qubits use checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)  |<span data-ttu-id="152ce-129">Hiermee wordt gecontroleerd of een bewerking wordt toegepast op een qubit die al is vrijgegeven</span><span class="sxs-lookup"><span data-stu-id="152ce-129">Checks if the program applies an operation to a qubit that is already released</span></span> |
|[<span data-ttu-id="152ce-130">Teller primitieve bewerkingen</span><span class="sxs-lookup"><span data-stu-id="152ce-130">Primitive operations counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)  | <span data-ttu-id="152ce-131">Telt het aantal primitieve bewerkingen dat wordt gebruikt door elke bewerking die wordt aangeroepen in een kwantumprogramma</span><span class="sxs-lookup"><span data-stu-id="152ce-131">Counts the number of primitives used by every operation invoked in a quantum program</span></span>  |
|[<span data-ttu-id="152ce-132">Diepteteller</span><span class="sxs-lookup"><span data-stu-id="152ce-132">Depth counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)  |<span data-ttu-id="152ce-133">Verzamelt aantallen die de ondergrens vertegenwoordigen van elke bewerking die wordt aangeroepen in een kwantumprogramma</span><span class="sxs-lookup"><span data-stu-id="152ce-133">Gathers counts that represent the lower bound of the depth of every operation invoked in a quantum program</span></span>   |
|[<span data-ttu-id="152ce-134">Breedteteller</span><span class="sxs-lookup"><span data-stu-id="152ce-134">Width counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)  |<span data-ttu-id="152ce-135">Telt het aantal qubits dat wordt toegewezen en uitgeleend door elke bewerking in een kwantumprogramma</span><span class="sxs-lookup"><span data-stu-id="152ce-135">Counts the number of qubits allocated and borrowed by each operation in a quantum program</span></span> |

<span data-ttu-id="152ce-136">Elk van deze hulpprogramma's wordt ingeschakeld door de juiste vlaggen in `QCTraceSimulatorConfiguration` in te stellen en de configuratie vervolgens door te geven aan de declaratie `QCTraceSimulator`.</span><span class="sxs-lookup"><span data-stu-id="152ce-136">Each of these tools is enabled by setting appropriate flags in `QCTraceSimulatorConfiguration` and then passing the configuration to the `QCTraceSimulator` declaration.</span></span> <span data-ttu-id="152ce-137">Raadpleeg de links in de voorgaande lijst voor meer informatie over het gebruik van deze hulpprogramma's.</span><span class="sxs-lookup"><span data-stu-id="152ce-137">For information on using each of these tools, see the links in the preceding list.</span></span> <span data-ttu-id="152ce-138">Raadpleeg [QCTraceSimulatorConfiguration](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) voor meer informatie over het configureren van `QCTraceSimulator`.</span><span class="sxs-lookup"><span data-stu-id="152ce-138">For more information about configuring `QCTraceSimulator`, see [QCTraceSimulatorConfiguration](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration).</span></span>

## <a name="qctracesimulator-methods"></a><span data-ttu-id="152ce-139">QCTraceSimulator-methoden</span><span class="sxs-lookup"><span data-stu-id="152ce-139">QCTraceSimulator methods</span></span>

<span data-ttu-id="152ce-140">`QCTraceSimulator` heeft verschillende ingebouwde methoden voor het ophalen van de waarden van de metrische gegevens die tijdens een kwantumbewerking worden bijgehouden.</span><span class="sxs-lookup"><span data-stu-id="152ce-140">`QCTraceSimulator` has several built-in methods to retrieve the values of the metrics tracked during a quantum operation.</span></span> <span data-ttu-id="152ce-141">Voorbeelden van de [QCTraceSimulator.GetMetric](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) en de methoden [QCTraceSimulator.ToCSV](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.tocsv) zijn te vinden in de artikelen [Teller voor primitieve bewerkingen](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter), [Diepteteller](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) en [Breedteteller](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter).</span><span class="sxs-lookup"><span data-stu-id="152ce-141">Examples of the [QCTraceSimulator.GetMetric](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) and the [QCTraceSimulator.ToCSV](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.tocsv) methods can be found in the [Primitive operations counter](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter), [Depth counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter), and [Width counter](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter) articles.</span></span> <span data-ttu-id="152ce-142">Zie [QCTraceSimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) in de API-verwijzing voor Q# voor meer informatie over alle beschikbare methoden.</span><span class="sxs-lookup"><span data-stu-id="152ce-142">For more information on all available methods, see [QCTraceSimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) in the Q# API reference.</span></span>  

## <a name="see-also"></a><span data-ttu-id="152ce-143">Zie ook</span><span class="sxs-lookup"><span data-stu-id="152ce-143">See also</span></span>

- [<span data-ttu-id="152ce-144">Kwantumresoure-estimator</span><span class="sxs-lookup"><span data-stu-id="152ce-144">Quantum resources estimator</span></span>](xref:microsoft.quantum.machines.resources-estimator)
- [<span data-ttu-id="152ce-145">Kwantum Toffoli-simulator</span><span class="sxs-lookup"><span data-stu-id="152ce-145">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="152ce-146">Kwantumsimulator voor volledige toestand</span><span class="sxs-lookup"><span data-stu-id="152ce-146">Quantum full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 