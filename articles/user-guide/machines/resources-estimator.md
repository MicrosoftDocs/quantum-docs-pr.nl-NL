---
title: Quantum bronnen Estimator-Quantum Development Kit
description: Meer informatie over de micro soft QDK resources Estimator, waarmee de resources die nodig zijn voor het uitvoeren van een bepaald exemplaar van een Q# bewerking op een quantum computer, worden geschat.
author: anpaz-msft
ms.author: anpaz
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
no-loc:
- Q#
- $$v
ms.openlocfilehash: 6138c098a4efe2797c7d7360573ddcb9cb70a6c1
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835924"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a><span data-ttu-id="ae0b7-103">QDK-resources (Quantum Development Kit) estimator</span><span class="sxs-lookup"><span data-stu-id="ae0b7-103">Quantum Development Kit (QDK) resources estimator</span></span>

<span data-ttu-id="ae0b7-104">Zoals de naam al aangeeft, `ResourcesEstimator` schat de klasse de resources die vereist zijn om een bepaald exemplaar van een Q# bewerking op een quantum computer uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-104">As the name implies, the `ResourcesEstimator` class estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span> <span data-ttu-id="ae0b7-105">Dit wordt bereikt door de Quantum bewerking uit te voeren zonder dat de status van een quantum computer werkelijk wordt gesimuleerd. Daarom schatten IT resources voor Q# bewerkingen die gebruikmaken van duizenden qubits, op voor waarde dat het klassieke deel van de code in een redelijke tijd wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-105">It accomplishes this by running the quantum operation without actually simulating the state of a quantum computer; for this reason, it estimates resources for Q# operations that use thousands of qubits, provided that the classical part of the code runs in a reasonable time.</span></span>

<span data-ttu-id="ae0b7-106">De bronnen Estimator is gebaseerd op de [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), die een uitgebreidere verzameling metrische gegevens en hulpprogram ma's biedt om fouten in Program ma's op te sporen Q# .</span><span class="sxs-lookup"><span data-stu-id="ae0b7-106">The resources estimator is built on top of the [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), which provides a richer set of metrics and tools to help debug Q# programs.</span></span>

## <a name="invoking-and-running-the-resources-estimator"></a><span data-ttu-id="ae0b7-107">De bronnen Estimator aanroepen en uitvoeren</span><span class="sxs-lookup"><span data-stu-id="ae0b7-107">Invoking and running the resources estimator</span></span>

<span data-ttu-id="ae0b7-108">U kunt de resources Estimator gebruiken om een wille keurige bewerking uit te voeren Q# .</span><span class="sxs-lookup"><span data-stu-id="ae0b7-108">You can use the resources estimator to run any Q# operation.</span></span> <span data-ttu-id="ae0b7-109">Zie [manieren om een Q# programma uit te voeren](xref:microsoft.quantum.guide.host-programs)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-109">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-resources-estimator-from-c"></a><span data-ttu-id="ae0b7-110">Aanroepen van de bronnen Estimator van C #</span><span class="sxs-lookup"><span data-stu-id="ae0b7-110">Invoking the resources estimator from C#</span></span> 

<span data-ttu-id="ae0b7-111">Net als bij andere doelmachines maakt u eerst een exemplaar van de klasse `ResourceEstimator` en geeft u deze vervolgens door als de eerste parameter van de methode `Run` van een bewerking.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-111">As with other target machines, you first create an instance of the `ResourceEstimator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="ae0b7-112">Houd er rekening mee dat, in tegenstelling tot de klasse `QuantumSimulator`, de klasse `ResourceEstimator` de interface <xref:System.IDisposable> niet implementeert, zodat u deze niet hoeft in te sluiten in een instructie `using`.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-112">Note that, unlike the `QuantumSimulator` class, the `ResourceEstimator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            ResourcesEstimator estimator = new ResourcesEstimator();
            MyQuantumProgram.Run(estimator).Wait();
            Console.WriteLine(estimator.ToTSV());
        }
    }
}
```

<span data-ttu-id="ae0b7-113">Zoals in het voor beeld wordt weer gegeven, `ResourcesEstimator` biedt de `ToTSV()` methode, waarmee een tabel wordt gegenereerd met door tabs gescheiden waarden (TSV).</span><span class="sxs-lookup"><span data-stu-id="ae0b7-113">As the example shows, `ResourcesEstimator` provides the `ToTSV()` method, which generates a table with tab-separated values (TSV).</span></span> <span data-ttu-id="ae0b7-114">U kunt de tabel opslaan in een bestand of weer geven in de-console voor analyse.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-114">You can save the table to a file or display it to the console for analysis.</span></span> <span data-ttu-id="ae0b7-115">Hier volgt een voor beeld van de uitvoer van het voor gaande programma:</span><span class="sxs-lookup"><span data-stu-id="ae0b7-115">The following is a sample output from the preceding program:</span></span>

```output
Metric          Sum
CNOT            1000
QubitClifford   1000
R               0
Measure         4002
T               0
Depth           0
Width           2
BorrowedWidth   0
```

> [!NOTE]
> <span data-ttu-id="ae0b7-116">`ResourcesEstimator`Bij elke uitvoering worden de berekeningen niet opnieuw door een exemplaar opnieuw ingesteld.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-116">A `ResourcesEstimator` instance does not reset its calculations on every run.</span></span> <span data-ttu-id="ae0b7-117">Als u hetzelfde exemplaar gebruikt om een andere bewerking uit te voeren, worden de nieuwe resultaten geaggregeerd met de bestaande resultaten.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-117">If you use the same instance to run another operation, it aggregates the new results with the existing results.</span></span> <span data-ttu-id="ae0b7-118">Als u berekeningen tussen uitvoeringen wilt resetten, maakt u voor elke uitvoering een nieuw exemplaar.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-118">If you need to reset calculations between runs, create a new instance for every run.</span></span>

### <a name="invoking-the-resources-estimator-from-python"></a><span data-ttu-id="ae0b7-119">De bronnen Estimator van python worden aangeroepen</span><span class="sxs-lookup"><span data-stu-id="ae0b7-119">Invoking the resources estimator from Python</span></span>

<span data-ttu-id="ae0b7-120">Gebruik de methode [estimate_resources ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) vanuit de python-bibliotheek met de geïmporteerde Q# bewerking:</span><span class="sxs-lookup"><span data-stu-id="ae0b7-120">Use the [estimate_resources()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) method from the Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.estimate_resources()
```

### <a name="invoking-the-resources-estimator-from-the-command-line"></a><span data-ttu-id="ae0b7-121">Aanroepen van de bronnen Estimator vanaf de opdracht regel</span><span class="sxs-lookup"><span data-stu-id="ae0b7-121">Invoking the resources estimator from the command line</span></span>

<span data-ttu-id="ae0b7-122">Wanneer u een Q# programma uitvoert vanaf de opdracht regel, gebruikt u de para meter **--Simulator** (of **-s** ) om de doel computer op te geven `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="ae0b7-122">When running a Q# program from the command line, use the **--simulator** (or **-s** shortcut) parameter to specify the `ResourcesEstimator` target machine.</span></span> <span data-ttu-id="ae0b7-123">Met de volgende opdracht voert u een programma uit met behulp van de resources Estimator:</span><span class="sxs-lookup"><span data-stu-id="ae0b7-123">The following command runs a program using the resources estimator:</span></span> 

```dotnetcli
dotnet run -s ResourcesEstimator
```

### <a name="invoking-the-resources-estimator-from-juptyer-notebooks"></a><span data-ttu-id="ae0b7-124">De bronnen Estimator van Juptyer-notebooks aanroepen</span><span class="sxs-lookup"><span data-stu-id="ae0b7-124">Invoking the resources estimator from Juptyer Notebooks</span></span>

<span data-ttu-id="ae0b7-125">Gebruik de I Q# Magic-opdracht [% schatting](xref:microsoft.quantum.iqsharp.magic-ref.simulate) om de bewerking uit te voeren Q# .</span><span class="sxs-lookup"><span data-stu-id="ae0b7-125">Use the IQ# magic command [%estimate](xref:microsoft.quantum.iqsharp.magic-ref.simulate) to run the Q# operation.</span></span>

```
%estimate myOperation
```

## <a name="programmatically-retrieving-the-estimated-data"></a><span data-ttu-id="ae0b7-126">De geschatte gegevens programmatisch ophalen</span><span class="sxs-lookup"><span data-stu-id="ae0b7-126">Programmatically retrieving the estimated data</span></span>

<span data-ttu-id="ae0b7-127">Naast een TSV-tabel kunt u de resources die zijn geschat tijdens de uitvoering programmatisch ophalen via de `Data` eigenschap van de resources Estimator.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-127">In addition to a TSV table, you can programmatically retrieve the resources estimated during the run via the `Data` property of the resources estimator.</span></span> <span data-ttu-id="ae0b7-128">De `Data` eigenschap levert een `System.DataTable` exemplaar met twee kolommen: `Metric` en `Sum` , geïndexeerd op basis van de namen van de metrische gegevens.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-128">The `Data` property provides a `System.DataTable` instance with two columns: `Metric` and `Sum`, indexed by the metrics' names.</span></span>

<span data-ttu-id="ae0b7-129">De volgende code laat zien hoe u het totale aantal `QubitClifford` `T` en de `CNOT` bewerkingen die worden gebruikt door een bewerking Q# kunt ophalen en afdrukken:</span><span class="sxs-lookup"><span data-stu-id="ae0b7-129">The following code shows how to retrieve and print the total number of `QubitClifford`, `T` and `CNOT` operations used by a Q# operation:</span></span>

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            ResourcesEstimator estimator = new ResourcesEstimator();
            MyQuantumProgram.Run(estimator).Wait();

            var data = estimator.Data;
            Console.WriteLine($"QubitCliffords: {data.Rows.Find("QubitClifford")["Sum"]}");
            Console.WriteLine($"Ts: {data.Rows.Find("T")["Sum"]}");
            Console.WriteLine($"CNOTs: {data.Rows.Find("CNOT")["Sum"]}");
        }
    }
}
```

## <a name="metrics-reported"></a><span data-ttu-id="ae0b7-130">Gemelde metrische gegevens</span><span class="sxs-lookup"><span data-stu-id="ae0b7-130">Metrics Reported</span></span>

<span data-ttu-id="ae0b7-131">De resources Estimator traceert de volgende metrische gegevens:</span><span class="sxs-lookup"><span data-stu-id="ae0b7-131">The resources estimator tracks the following metrics:</span></span>

|<span data-ttu-id="ae0b7-132">Gegevens</span><span class="sxs-lookup"><span data-stu-id="ae0b7-132">Metric</span></span>|<span data-ttu-id="ae0b7-133">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ae0b7-133">Description</span></span>|
|----|----|
|<span data-ttu-id="ae0b7-134">__CNOT__</span><span class="sxs-lookup"><span data-stu-id="ae0b7-134">__CNOT__</span></span>    |<span data-ttu-id="ae0b7-135">Het aantal uitgevoerde `CNOT` bewerkingen (ook wel beheerde Pauli X-bewerkingen genoemd).</span><span class="sxs-lookup"><span data-stu-id="ae0b7-135">The run count of `CNOT` operations (also known as Controlled Pauli X operations).</span></span>|
|<span data-ttu-id="ae0b7-136">__QubitClifford__</span><span class="sxs-lookup"><span data-stu-id="ae0b7-136">__QubitClifford__</span></span> |<span data-ttu-id="ae0b7-137">Het aantal uitvoeringen van een afzonderlijke Qubit-Clifford-en Pauli-bewerking.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-137">The run count of any single qubit Clifford and Pauli operations.</span></span>|
|<span data-ttu-id="ae0b7-138">__Measure__</span><span class="sxs-lookup"><span data-stu-id="ae0b7-138">__Measure__</span></span>    |<span data-ttu-id="ae0b7-139">Het aantal uitvoeringen van een wille keurige meting.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-139">The run count of any measurements.</span></span>  |
|<span data-ttu-id="ae0b7-140">__R__</span><span class="sxs-lookup"><span data-stu-id="ae0b7-140">__R__</span></span>    |<span data-ttu-id="ae0b7-141">Het aantal uitvoeringen van een Qubit draaiing, met uitzonde ring van `T` Clifford-en Pauli-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-141">The run count of any single-qubit rotations, excluding `T`, Clifford and Pauli operations.</span></span>  |
|<span data-ttu-id="ae0b7-142">__T__</span><span class="sxs-lookup"><span data-stu-id="ae0b7-142">__T__</span></span>    |<span data-ttu-id="ae0b7-143">Het aantal uitvoeringen van `T` bewerkingen en hun conjugaat, waaronder de `T` bewerkingen, T_x = h. t. h en T_y = hy. t. hy.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-143">The run count of `T` operations and their conjugates, including the `T` operations, T_x = H.T.H, and T_y = Hy.T.Hy.</span></span>  |
|<span data-ttu-id="ae0b7-144">__Diepga__</span><span class="sxs-lookup"><span data-stu-id="ae0b7-144">__Depth__</span></span>|<span data-ttu-id="ae0b7-145">De ondergrens voor de diepte van het Quantum circuit dat door de bewerking wordt uitgevoerd Q# .</span><span class="sxs-lookup"><span data-stu-id="ae0b7-145">The lower bound for the depth of the quantum circuit run by the Q# operation.</span></span> <span data-ttu-id="ae0b7-146">Standaard telt alleen Gates over de diepte waarde `T` .</span><span class="sxs-lookup"><span data-stu-id="ae0b7-146">By default, the depth metric only counts `T` gates.</span></span> <span data-ttu-id="ae0b7-147">Zie [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-147">For more details, see [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span></span>   |
|<span data-ttu-id="ae0b7-148">__Breedte__</span><span class="sxs-lookup"><span data-stu-id="ae0b7-148">__Width__</span></span>    |<span data-ttu-id="ae0b7-149">De ondergrens voor het maximum aantal toegewezen qubits tijdens het uitvoeren van de Q# bewerking.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-149">The lower bound for the maximum number of qubits allocated during the run of the Q# operation.</span></span> <span data-ttu-id="ae0b7-150">Het is misschien niet mogelijk om tegelijkertijd zowel de __diepte__ als de __breedte__ van de ondergrenzen te verminderen.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-150">It might not be possible to achieve both __Depth__ and __Width__ lower bounds simultaneously.</span></span>  |
|<span data-ttu-id="ae0b7-151">__BorrowedWidth__</span><span class="sxs-lookup"><span data-stu-id="ae0b7-151">__BorrowedWidth__</span></span>    |<span data-ttu-id="ae0b7-152">Het maximale aantal qubits dat in de bewerking is geleend Q# .</span><span class="sxs-lookup"><span data-stu-id="ae0b7-152">The maximum number of qubits borrowed inside the Q# operation.</span></span>  |

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="ae0b7-153">De waarschijnlijkheid van metingsresultaten opgeven</span><span class="sxs-lookup"><span data-stu-id="ae0b7-153">Providing the probability of measurement outcomes</span></span>

<span data-ttu-id="ae0b7-154">U kunt <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> uit de <xref:microsoft.quantum.diagnostics> naam ruimte gebruiken om informatie te geven over de verwachte waarschijnlijkheid van een meting bewerking.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-154">You can use <xref:microsoft.quantum.diagnostics.assertmeasurementprobability> from the <xref:microsoft.quantum.diagnostics> namespace to provide information about the expected probability of a measurement operation.</span></span> <span data-ttu-id="ae0b7-155">Zie [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ae0b7-155">For more information, see [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)</span></span>

## <a name="see-also"></a><span data-ttu-id="ae0b7-156">Zie tevens</span><span class="sxs-lookup"><span data-stu-id="ae0b7-156">See also</span></span>

- [<span data-ttu-id="ae0b7-157">Quantum Trace Simulator</span><span class="sxs-lookup"><span data-stu-id="ae0b7-157">Quantum trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [<span data-ttu-id="ae0b7-158">Kwantum Toffoli-simulator</span><span class="sxs-lookup"><span data-stu-id="ae0b7-158">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="ae0b7-159">Kwantumsimulator voor volledige toestand</span><span class="sxs-lookup"><span data-stu-id="ae0b7-159">Quantum full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 