---
title: Quantum bronnen Estimator-Quantum Development Kit
description: 'Meer informatie over de micro soft QDK resources Estimator, waarmee de resources die nodig zijn voor het uitvoeren van een bepaald exemplaar van een Q# bewerking op een quantum computer, worden geschat.'
author: anpaz-msft
ms.author: anpaz
ms.date: 06/26/2020
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
no-loc:
- 'Q#'
- '$$v'
ms.openlocfilehash: e1ec01d85a141b9c8a7a5ba5589663a0773520e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691878"
---
# <a name="quantum-development-kit-qdk-resources-estimator"></a><span data-ttu-id="8f065-103">QDK-resources (Quantum Development Kit) estimator</span><span class="sxs-lookup"><span data-stu-id="8f065-103">Quantum Development Kit (QDK) resources estimator</span></span>

<span data-ttu-id="8f065-104">Zoals de naam al aangeeft, `ResourcesEstimator` schat de klasse de resources die vereist zijn om een bepaald exemplaar van een Q# bewerking op een quantum computer uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="8f065-104">As the name implies, the `ResourcesEstimator` class estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span> <span data-ttu-id="8f065-105">Dit wordt bereikt door de Quantum bewerking uit te voeren zonder dat de status van een quantum computer werkelijk wordt gesimuleerd. Daarom schatten IT resources voor Q# bewerkingen die gebruikmaken van duizenden qubits, op voor waarde dat het klassieke deel van de code in een redelijke tijd wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="8f065-105">It accomplishes this by running the quantum operation without actually simulating the state of a quantum computer; for this reason, it estimates resources for Q# operations that use thousands of qubits, provided that the classical part of the code runs in a reasonable time.</span></span>

<span data-ttu-id="8f065-106">De bronnen Estimator is gebaseerd op de [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), die een uitgebreidere verzameling metrische gegevens en hulpprogram ma's biedt om fouten in Program ma's op te sporen Q# .</span><span class="sxs-lookup"><span data-stu-id="8f065-106">The resources estimator is built on top of the [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), which provides a richer set of metrics and tools to help debug Q# programs.</span></span>

## <a name="invoking-and-running-the-resources-estimator"></a><span data-ttu-id="8f065-107">De bronnen Estimator aanroepen en uitvoeren</span><span class="sxs-lookup"><span data-stu-id="8f065-107">Invoking and running the resources estimator</span></span>

<span data-ttu-id="8f065-108">U kunt de resources Estimator gebruiken om een wille keurige bewerking uit te voeren Q# .</span><span class="sxs-lookup"><span data-stu-id="8f065-108">You can use the resources estimator to run any Q# operation.</span></span> <span data-ttu-id="8f065-109">Zie [manieren om een Q# programma uit te voeren](xref:microsoft.quantum.guide.host-programs)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8f065-109">For additional details, see [Ways to run a Q# program](xref:microsoft.quantum.guide.host-programs).</span></span>

### <a name="invoking-the-resources-estimator-from-c"></a><span data-ttu-id="8f065-110">Aanroepen van de bronnen Estimator van C #</span><span class="sxs-lookup"><span data-stu-id="8f065-110">Invoking the resources estimator from C#</span></span> 

<span data-ttu-id="8f065-111">Net als bij andere doelmachines maakt u eerst een exemplaar van de klasse `ResourceEstimator` en geeft u deze vervolgens door als de eerste parameter van de methode `Run` van een bewerking.</span><span class="sxs-lookup"><span data-stu-id="8f065-111">As with other target machines, you first create an instance of the `ResourceEstimator` class and then pass it as the first parameter of an operation's `Run` method.</span></span>

<span data-ttu-id="8f065-112">Houd er rekening mee dat, in tegenstelling tot de klasse `QuantumSimulator`, de klasse `ResourceEstimator` de interface <xref:System.IDisposable> niet implementeert, zodat u deze niet hoeft in te sluiten in een instructie `using`.</span><span class="sxs-lookup"><span data-stu-id="8f065-112">Note that, unlike the `QuantumSimulator` class, the `ResourceEstimator` class does not implement the <xref:System.IDisposable> interface, and thus you do not need to enclose it within a `using` statement.</span></span>

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

<span data-ttu-id="8f065-113">Zoals in het voor beeld wordt weer gegeven, `ResourcesEstimator` biedt de `ToTSV()` methode, waarmee een tabel wordt gegenereerd met door tabs gescheiden waarden (TSV).</span><span class="sxs-lookup"><span data-stu-id="8f065-113">As the example shows, `ResourcesEstimator` provides the `ToTSV()` method, which generates a table with tab-separated values (TSV).</span></span> <span data-ttu-id="8f065-114">U kunt de tabel opslaan in een bestand of weer geven in de-console voor analyse.</span><span class="sxs-lookup"><span data-stu-id="8f065-114">You can save the table to a file or display it to the console for analysis.</span></span> <span data-ttu-id="8f065-115">Hier volgt een voor beeld van de uitvoer van het voor gaande programma:</span><span class="sxs-lookup"><span data-stu-id="8f065-115">The following is a sample output from the preceding program:</span></span>

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
> <span data-ttu-id="8f065-116">`ResourcesEstimator`Bij elke uitvoering worden de berekeningen niet opnieuw door een exemplaar opnieuw ingesteld.</span><span class="sxs-lookup"><span data-stu-id="8f065-116">A `ResourcesEstimator` instance does not reset its calculations on every run.</span></span> <span data-ttu-id="8f065-117">Als u hetzelfde exemplaar gebruikt om een andere bewerking uit te voeren, worden de nieuwe resultaten geaggregeerd met de bestaande resultaten.</span><span class="sxs-lookup"><span data-stu-id="8f065-117">If you use the same instance to run another operation, it aggregates the new results with the existing results.</span></span> <span data-ttu-id="8f065-118">Als u berekeningen tussen uitvoeringen wilt resetten, maakt u voor elke uitvoering een nieuw exemplaar.</span><span class="sxs-lookup"><span data-stu-id="8f065-118">If you need to reset calculations between runs, create a new instance for every run.</span></span>

### <a name="invoking-the-resources-estimator-from-python"></a><span data-ttu-id="8f065-119">De bronnen Estimator van python worden aangeroepen</span><span class="sxs-lookup"><span data-stu-id="8f065-119">Invoking the resources estimator from Python</span></span>

<span data-ttu-id="8f065-120">Gebruik de methode [estimate_resources ()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) vanuit de python-bibliotheek met de geïmporteerde Q# bewerking:</span><span class="sxs-lookup"><span data-stu-id="8f065-120">Use the [estimate_resources()](https://docs.microsoft.com/python/qsharp-core/qsharp.loader.qsharpcallable) method from the Python library with the imported Q# operation:</span></span>

```python
qubit_result = myOperation.estimate_resources()
```

### <a name="invoking-the-resources-estimator-from-the-command-line"></a><span data-ttu-id="8f065-121">Aanroepen van de bronnen Estimator vanaf de opdracht regel</span><span class="sxs-lookup"><span data-stu-id="8f065-121">Invoking the resources estimator from the command line</span></span>

<span data-ttu-id="8f065-122">Wanneer u een Q# programma uitvoert vanaf de opdracht regel, gebruikt u de para meter **--Simulator** (of **-s** ) om de doel computer op te geven `ResourcesEstimator` .</span><span class="sxs-lookup"><span data-stu-id="8f065-122">When running a Q# program from the command line, use the **--simulator** (or **-s** shortcut) parameter to specify the `ResourcesEstimator` target machine.</span></span> <span data-ttu-id="8f065-123">Met de volgende opdracht voert u een programma uit met behulp van de resources Estimator:</span><span class="sxs-lookup"><span data-stu-id="8f065-123">The following command runs a program using the resources estimator:</span></span> 

```dotnetcli
dotnet run -s ResourcesEstimator
```

### <a name="invoking-the-resources-estimator-from-juptyer-notebooks"></a><span data-ttu-id="8f065-124">De bronnen Estimator van Juptyer-notebooks aanroepen</span><span class="sxs-lookup"><span data-stu-id="8f065-124">Invoking the resources estimator from Juptyer Notebooks</span></span>

<span data-ttu-id="8f065-125">Gebruik de I Q# Magic-opdracht [% schatting](xref:microsoft.quantum.iqsharp.magic-ref.simulate) om de bewerking uit te voeren Q# .</span><span class="sxs-lookup"><span data-stu-id="8f065-125">Use the IQ# magic command [%estimate](xref:microsoft.quantum.iqsharp.magic-ref.simulate) to run the Q# operation.</span></span>

```
%estimate myOperation
```

## <a name="programmatically-retrieving-the-estimated-data"></a><span data-ttu-id="8f065-126">De geschatte gegevens programmatisch ophalen</span><span class="sxs-lookup"><span data-stu-id="8f065-126">Programmatically retrieving the estimated data</span></span>

<span data-ttu-id="8f065-127">Naast een TSV-tabel kunt u de resources die zijn geschat tijdens de uitvoering programmatisch ophalen via de `Data` eigenschap van de resources Estimator.</span><span class="sxs-lookup"><span data-stu-id="8f065-127">In addition to a TSV table, you can programmatically retrieve the resources estimated during the run via the `Data` property of the resources estimator.</span></span> <span data-ttu-id="8f065-128">De `Data` eigenschap levert een `System.DataTable` exemplaar met twee kolommen: `Metric` en `Sum` , geïndexeerd op basis van de namen van de metrische gegevens.</span><span class="sxs-lookup"><span data-stu-id="8f065-128">The `Data` property provides a `System.DataTable` instance with two columns: `Metric` and `Sum`, indexed by the metrics' names.</span></span>

<span data-ttu-id="8f065-129">De volgende code laat zien hoe u het totale aantal `QubitClifford` `T` en de `CNOT` bewerkingen die worden gebruikt door een bewerking Q# kunt ophalen en afdrukken:</span><span class="sxs-lookup"><span data-stu-id="8f065-129">The following code shows how to retrieve and print the total number of `QubitClifford`, `T` and `CNOT` operations used by a Q# operation:</span></span>

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

## <a name="metrics-reported"></a><span data-ttu-id="8f065-130">Gemelde metrische gegevens</span><span class="sxs-lookup"><span data-stu-id="8f065-130">Metrics Reported</span></span>

<span data-ttu-id="8f065-131">De resources Estimator traceert de volgende metrische gegevens:</span><span class="sxs-lookup"><span data-stu-id="8f065-131">The resources estimator tracks the following metrics:</span></span>

|<span data-ttu-id="8f065-132">Gegevens</span><span class="sxs-lookup"><span data-stu-id="8f065-132">Metric</span></span>|<span data-ttu-id="8f065-133">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8f065-133">Description</span></span>|
|----|----|
|<span data-ttu-id="8f065-134">__CNOT__</span><span class="sxs-lookup"><span data-stu-id="8f065-134">__CNOT__</span></span>    |<span data-ttu-id="8f065-135">Het aantal uitgevoerde `CNOT` bewerkingen (ook wel beheerde Pauli X-bewerkingen genoemd).</span><span class="sxs-lookup"><span data-stu-id="8f065-135">The run count of `CNOT` operations (also known as Controlled Pauli X operations).</span></span>|
|<span data-ttu-id="8f065-136">__QubitClifford__</span><span class="sxs-lookup"><span data-stu-id="8f065-136">__QubitClifford__</span></span> |<span data-ttu-id="8f065-137">Het aantal uitvoeringen van een afzonderlijke Qubit-Clifford-en Pauli-bewerking.</span><span class="sxs-lookup"><span data-stu-id="8f065-137">The run count of any single qubit Clifford and Pauli operations.</span></span>|
|<span data-ttu-id="8f065-138">__Measure__</span><span class="sxs-lookup"><span data-stu-id="8f065-138">__Measure__</span></span>    |<span data-ttu-id="8f065-139">Het aantal uitvoeringen van een wille keurige meting.</span><span class="sxs-lookup"><span data-stu-id="8f065-139">The run count of any measurements.</span></span>  |
|<span data-ttu-id="8f065-140">__R__</span><span class="sxs-lookup"><span data-stu-id="8f065-140">__R__</span></span>    |<span data-ttu-id="8f065-141">Het aantal uitvoeringen van een Qubit draaiing, met uitzonde ring van `T` Clifford-en Pauli-bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="8f065-141">The run count of any single-qubit rotations, excluding `T`, Clifford and Pauli operations.</span></span>  |
|<span data-ttu-id="8f065-142">__T__</span><span class="sxs-lookup"><span data-stu-id="8f065-142">__T__</span></span>    |<span data-ttu-id="8f065-143">Het aantal uitvoeringen van `T` bewerkingen en hun conjugaat, waaronder de `T` bewerkingen, T_x = h. t. h en T_y = hy. t. hy.</span><span class="sxs-lookup"><span data-stu-id="8f065-143">The run count of `T` operations and their conjugates, including the `T` operations, T_x = H.T.H, and T_y = Hy.T.Hy.</span></span>  |
|<span data-ttu-id="8f065-144">__Diepga__</span><span class="sxs-lookup"><span data-stu-id="8f065-144">__Depth__</span></span>|<span data-ttu-id="8f065-145">Diepte van het Quantum circuit dat door de Q# bewerking wordt uitgevoerd (Zie [hieronder](#depth-width-and-qubitcount)).</span><span class="sxs-lookup"><span data-stu-id="8f065-145">Depth of the quantum circuit run by the Q# operation (see [below](#depth-width-and-qubitcount)).</span></span> <span data-ttu-id="8f065-146">Standaard telt alleen Gates over de diepte waarde `T` .</span><span class="sxs-lookup"><span data-stu-id="8f065-146">By default, the depth metric only counts `T` gates.</span></span> <span data-ttu-id="8f065-147">Zie [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8f065-147">For more details, see [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span></span>   |
|<span data-ttu-id="8f065-148">__Breedte__</span><span class="sxs-lookup"><span data-stu-id="8f065-148">__Width__</span></span>|<span data-ttu-id="8f065-149">De breedte van het Quantum circuit dat door de bewerking wordt uitgevoerd Q# (Zie [hieronder](#depth-width-and-qubitcount)).</span><span class="sxs-lookup"><span data-stu-id="8f065-149">Width of the quantum circuit run by the Q# operation (see [below](#depth-width-and-qubitcount)).</span></span> <span data-ttu-id="8f065-150">Standaard telt alleen Gates over de diepte waarde `T` .</span><span class="sxs-lookup"><span data-stu-id="8f065-150">By default, the depth metric only counts `T` gates.</span></span> <span data-ttu-id="8f065-151">Zie [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8f065-151">For more details, see [Depth Counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter).</span></span>   |
|<span data-ttu-id="8f065-152">__QubitCount__</span><span class="sxs-lookup"><span data-stu-id="8f065-152">__QubitCount__</span></span>    |<span data-ttu-id="8f065-153">De ondergrens voor het maximum aantal toegewezen qubits tijdens het uitvoeren van de Q# bewerking.</span><span class="sxs-lookup"><span data-stu-id="8f065-153">The lower bound for the maximum number of qubits allocated during the run of the Q# operation.</span></span> <span data-ttu-id="8f065-154">Deze metrische gegevens zijn mogelijk niet compatibel met de __diepte__ (zie hieronder).</span><span class="sxs-lookup"><span data-stu-id="8f065-154">This metric might not be compatible with __Depth__ (see below).</span></span>  |
|<span data-ttu-id="8f065-155">__BorrowedWidth__</span><span class="sxs-lookup"><span data-stu-id="8f065-155">__BorrowedWidth__</span></span>    |<span data-ttu-id="8f065-156">Het maximale aantal qubits dat in de bewerking is geleend Q# .</span><span class="sxs-lookup"><span data-stu-id="8f065-156">The maximum number of qubits borrowed inside the Q# operation.</span></span>  |


## <a name="depth-width-and-qubitcount"></a><span data-ttu-id="8f065-157">Diepte, breedte en QubitCount</span><span class="sxs-lookup"><span data-stu-id="8f065-157">Depth, Width, and QubitCount</span></span>

<span data-ttu-id="8f065-158">De gerapporteerde diepte-en breedte schattingen zijn compatibel met elkaar.</span><span class="sxs-lookup"><span data-stu-id="8f065-158">Reported Depth and Width estimates are compatible with each other.</span></span>
<span data-ttu-id="8f065-159">(Voorheen zijn beide nummers haalbaar, maar er zijn verschillende circuits vereist voor diepte en breedte.) Momenteel kunnen beide metrische gegevens in dit paar tegelijk worden bereikt door hetzelfde circuit.</span><span class="sxs-lookup"><span data-stu-id="8f065-159">(Previously both numbers were achievable, but different circuits would be required for Depth and for Width.) Currently both metrics in this pair can be achieved by the same circuit at the same time.</span></span>

<span data-ttu-id="8f065-160">De volgende metrische gegevens worden gerapporteerd:</span><span class="sxs-lookup"><span data-stu-id="8f065-160">The following metrics are reported:</span></span>

<span data-ttu-id="8f065-161">__Diepte:__ Voor het uitvoeren van de bewerking-tijd die nodig is om het uit te voeren, wordt uitgegaan van specifieke Gate-tijden.</span><span class="sxs-lookup"><span data-stu-id="8f065-161">__Depth:__ For the root operation - time it takes to execute it assuming specific gate times.</span></span>
<span data-ttu-id="8f065-162">Voor bewerkingen die worden aangeroepen of een volgend verwerkings tijd verschil tussen de meest recente Qubit-beschikbaarheids tijd aan het begin en het einde van de bewerking.</span><span class="sxs-lookup"><span data-stu-id="8f065-162">For operations called or subsequent operations - time difference between latest qubit availability time at the beginning and the end of the operation.</span></span>

<span data-ttu-id="8f065-163">__Breedte:__ Voor het hoofd bewerking-aantal qubits dat daad werkelijk wordt gebruikt om het uit te voeren (en de bewerking te starten).</span><span class="sxs-lookup"><span data-stu-id="8f065-163">__Width:__ For the root operation - number of qubits actually used to execute it (and operation it calls).</span></span>
<span data-ttu-id="8f065-164">Voor bewerkingen die of volgende bewerkingen worden uitgevoerd, is het aantal meer qubits gebruikt naast de qubits die al aan het begin van de bewerking worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="8f065-164">For operations called or subsequent operations - how many more qubits were used in addition to the qubits already used at the beginning of the operation.</span></span>

<span data-ttu-id="8f065-165">Houd er rekening mee dat de hergebruikte qubits geen bijdrage levert aan dit aantal.</span><span class="sxs-lookup"><span data-stu-id="8f065-165">Please note, that reused qubits do not contribute to this number.</span></span>
<span data-ttu-id="8f065-166">Dat wil zeggen dat een aantal qubits is vrijgegeven voordat een start werd uitgevoerd en dat alle Qubit die door deze bewerking zijn gevraagd A (en de bewerkingen van A) zijn voldaan door eerdere release-qubits opnieuw te gebruiken, de breedte van bewerking A wordt gerapporteerd als 0.</span><span class="sxs-lookup"><span data-stu-id="8f065-166">I.e. if a few qubits have been released before operation A starts, and all qubit demanded by this operation A (and operations called from A) were satisfied by reusing previously release qubits, the Width of operation A is reported as 0.</span></span> <span data-ttu-id="8f065-167">Qubits is een bijdrage leveren aan de breedte.</span><span class="sxs-lookup"><span data-stu-id="8f065-167">Successfully borrowed qubits do not contribute to the Width either.</span></span>

<span data-ttu-id="8f065-168">__QubitCount:__ Voor de hoofd bewerking-minimum aantal qubits dat voldoende is om deze bewerking uit te voeren (en de bewerkingen zijn aangeroepen).</span><span class="sxs-lookup"><span data-stu-id="8f065-168">__QubitCount:__ For the root operation - minimum number of qubits that would be sufficient to execute this operation (and operations called from it).</span></span>
<span data-ttu-id="8f065-169">Voor bewerkingen met de naam of de volgende bewerkingen-minimum aantal qubits dat voldoende is om deze bewerking afzonderlijk uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="8f065-169">For operations called or subsequent operations - minimum number of qubits that would be sufficient to execute this operation separately.</span></span> <span data-ttu-id="8f065-170">Dit nummer bevat geen invoer qubits.</span><span class="sxs-lookup"><span data-stu-id="8f065-170">This number doesn't include input qubits.</span></span> <span data-ttu-id="8f065-171">Dit omvat gelede qubits.</span><span class="sxs-lookup"><span data-stu-id="8f065-171">It does include borrowed qubits.</span></span>

<span data-ttu-id="8f065-172">Twee bewerkings modi worden ondersteund.</span><span class="sxs-lookup"><span data-stu-id="8f065-172">Two modes of operation are supported.</span></span> <span data-ttu-id="8f065-173">De modus wordt geselecteerd door QCTraceSimulatorConfiguration. OptimizeDepth in te stellen.</span><span class="sxs-lookup"><span data-stu-id="8f065-173">Mode is selected by setting QCTraceSimulatorConfiguration.OptimizeDepth.</span></span>

<span data-ttu-id="8f065-174">__OptimizeDepth = True:__ QubitManager wordt ontmoedigd bij het opnieuw gebruiken van Qubit en wijst nieuwe Qubit toe elke keer dat deze wordt gevraagd voor een Qubit.</span><span class="sxs-lookup"><span data-stu-id="8f065-174">__OptimizeDepth=true:__ QubitManager is discouraged from qubit reuse and allocates new qubit every time it is asked for a qubit.</span></span> <span data-ttu-id="8f065-175">De __diepte__ van de hoofd bewerking wordt de minimale diepte (ondergrens).</span><span class="sxs-lookup"><span data-stu-id="8f065-175">For the root operation __Depth__ becomes the minimum depth (lower bound).</span></span> <span data-ttu-id="8f065-176">Er wordt voor deze diepte een compatibele __breedte__ gerapporteerd (beide kunnen tegelijkertijd worden bereikt).</span><span class="sxs-lookup"><span data-stu-id="8f065-176">Compatible __Width__ is reported for this depth (both can be achieved at the same time).</span></span> <span data-ttu-id="8f065-177">Houd er rekening mee dat deze breedte waarschijnlijk niet optimaal is op basis van deze diepte.</span><span class="sxs-lookup"><span data-stu-id="8f065-177">Note, that this width will likely be not optimal given this depth.</span></span> <span data-ttu-id="8f065-178">__QubitCount__ kan kleiner zijn dan de breedte voor de hoofd bewerking, omdat het opnieuw wordt aangenomen.</span><span class="sxs-lookup"><span data-stu-id="8f065-178">__QubitCount__ may be lower than Width for the root operation because it assumes reuse.</span></span>

<span data-ttu-id="8f065-179">__OptimizeDepth = False:__ QubitManager wordt aangemoedigd om qubits opnieuw te gebruiken en om vrijgegeven qubits te hergebruiken voordat nieuwe objecten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="8f065-179">__OptimizeDepth=false:__ QubitManager is encouraged to reuse qubits and will reuse released qubits before allocating new ones.</span></span> <span data-ttu-id="8f065-180">De __breedte__ van de hoofd bewerking wordt de minimale breedte (ondergrens).</span><span class="sxs-lookup"><span data-stu-id="8f065-180">For the root operation __Width__ becomes the minimal width (lower bound).</span></span> <span data-ttu-id="8f065-181">Er wordt een compatibele __diepte__ gerapporteerd waarop het kan worden bereikt.</span><span class="sxs-lookup"><span data-stu-id="8f065-181">Compatible __Depth__ is reported on which it can be achieved.</span></span> <span data-ttu-id="8f065-182">__QubitCount__ is hetzelfde als de __breedte__ voor de hoofd bewerking, uitgaande van geen leningen.</span><span class="sxs-lookup"><span data-stu-id="8f065-182">__QubitCount__ will be the same as __Width__ for the root operation assuming no borrowing.</span></span>

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="8f065-183">De waarschijnlijkheid van metingsresultaten opgeven</span><span class="sxs-lookup"><span data-stu-id="8f065-183">Providing the probability of measurement outcomes</span></span>

<span data-ttu-id="8f065-184">U kunt <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> uit de <xref:Microsoft.Quantum.Diagnostics> naam ruimte gebruiken om informatie te geven over de verwachte waarschijnlijkheid van een meting bewerking.</span><span class="sxs-lookup"><span data-stu-id="8f065-184">You can use <xref:Microsoft.Quantum.Diagnostics.AssertMeasurementProbability> from the <xref:Microsoft.Quantum.Diagnostics> namespace to provide information about the expected probability of a measurement operation.</span></span> <span data-ttu-id="8f065-185">Zie [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="8f065-185">For more information, see [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro)</span></span>

## <a name="see-also"></a><span data-ttu-id="8f065-186">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8f065-186">See also</span></span>

- [<span data-ttu-id="8f065-187">Quantum Trace Simulator</span><span class="sxs-lookup"><span data-stu-id="8f065-187">Quantum trace simulator</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.intro)
- [<span data-ttu-id="8f065-188">Kwantum Toffoli-simulator</span><span class="sxs-lookup"><span data-stu-id="8f065-188">Quantum Toffoli simulator</span></span>](xref:microsoft.quantum.machines.toffoli-simulator)
- [<span data-ttu-id="8f065-189">Kwantumsimulator voor volledige toestand</span><span class="sxs-lookup"><span data-stu-id="8f065-189">Quantum full state simulator</span></span>](xref:microsoft.quantum.machines.full-state-simulator) 
