---
title: Bronnen over de Quantum Development Kit estimator | Microsoft Docs
description: Overzicht van de resources van de Quantum Development Kit van micro soft estimator
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 1/22/2019
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: 591e306b3001934bd81342a533e3f6ca25129781
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184981"
---
# <a name="the-resourcesestimator-target-machine"></a><span data-ttu-id="7232e-103">De doel computer van de ResourcesEstimator</span><span class="sxs-lookup"><span data-stu-id="7232e-103">The ResourcesEstimator Target Machine</span></span>

<span data-ttu-id="7232e-104">Zoals de naam al aangeeft, schat het `ResourcesEstimator` de resources die nodig zijn om een bepaald exemplaar van een Q #-bewerking uit te voeren op een quantum computer.</span><span class="sxs-lookup"><span data-stu-id="7232e-104">As the name implies, the `ResourcesEstimator` estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>
<span data-ttu-id="7232e-105">Dit wordt bereikt door de Quantum bewerking uit te voeren zonder dat de status van een quantum computer werkelijk wordt gesimuleerd. Daarom kunnen er resources worden geschat voor Q #-bewerkingen die gebruikmaken van duizenden qubits.</span><span class="sxs-lookup"><span data-stu-id="7232e-105">It accomplishes this by executing the quantum operation without actually simulating the state of a quantum computer; for this reason, it can estimate resources for Q# operations that use thousands of qubits.</span></span>

## <a name="usage"></a><span data-ttu-id="7232e-106">Gebruik</span><span class="sxs-lookup"><span data-stu-id="7232e-106">Usage</span></span>

<span data-ttu-id="7232e-107">De `ResourcesEstimator` is maar een ander type doel computer, zodat deze kan worden gebruikt om elke Q #-bewerking uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="7232e-107">The `ResourcesEstimator` is just another type of target machine, thus it can be used to run any Q# operation.</span></span> 

<span data-ttu-id="7232e-108">Als andere doel machines kunt u deze gebruiken voor een C# hostprogramma een exemplaar maken en dit door geven als de eerste para meter van de `Run` methode van de bewerking:</span><span class="sxs-lookup"><span data-stu-id="7232e-108">As other target machines, to use it on a C# host program create an instance and pass it as the first parameter of the operation's `Run` method:</span></span>

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

<span data-ttu-id="7232e-109">Zoals in het voor beeld wordt weer gegeven, biedt de `ResourcesEstimator` een `ToTSV()` methode voor het genereren van een tabel met tab-gescheiden waarden (TSV) die in een bestand kunnen worden opgeslagen of naar de console worden geschreven voor analyse.</span><span class="sxs-lookup"><span data-stu-id="7232e-109">As the example shows, the `ResourcesEstimator` provides a `ToTSV()` method to generate a table with tab-seperated-values (TSV) that can be saved into a file or written to the console for analysis.</span></span> <span data-ttu-id="7232e-110">De uitvoer van het bovenstaande programma moet er ongeveer als volgt uitzien:</span><span class="sxs-lookup"><span data-stu-id="7232e-110">The output of the above program should look something like this:</span></span>

```Output
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
> <span data-ttu-id="7232e-111">Met de `ResourcesEstimator` worden de berekeningen bij elke uitvoering niet opnieuw ingesteld, als hetzelfde exemplaar wordt gebruikt om een andere bewerking uit te voeren, wordt het samen voegen van het aantal bestaande resultaten bewaard.</span><span class="sxs-lookup"><span data-stu-id="7232e-111">The `ResourcesEstimator` does not reset its calculations on every run, if the same instance is used to execute another operation it will keep aggregating counts on top of existing results.</span></span>
> <span data-ttu-id="7232e-112">Als u berekeningen tussen uitvoeringen wilt resetten, maakt u voor elke uitvoering een nieuw exemplaar.</span><span class="sxs-lookup"><span data-stu-id="7232e-112">If you need to reset calculations between runs, create a new instance for every execution.</span></span>


## <a name="programmatically-retrieving-the-estimated-data"></a><span data-ttu-id="7232e-113">De geschatte gegevens programmatisch ophalen</span><span class="sxs-lookup"><span data-stu-id="7232e-113">Programmatically Retrieving the Estimated Data</span></span>

<span data-ttu-id="7232e-114">Naast een TSV-tabel kunnen de geschatte resources via een programma worden opgehaald via de eigenschap `Data` van de `ResourcesEstimator`.</span><span class="sxs-lookup"><span data-stu-id="7232e-114">In addition to a TSV table, the resources estimated can be retrieved programmatically via the `ResourcesEstimator`'s `Data` property.</span></span> <span data-ttu-id="7232e-115">`Data` levert een `System.DataTable`-exemplaar met twee kolommen: `Metric` en `Sum`, geïndexeerd op basis van de namen van metrische gegevens.</span><span class="sxs-lookup"><span data-stu-id="7232e-115">`Data` provides a `System.DataTable` instance with two columns: `Metric` and `Sum`, indexed by the metrics names.</span></span>

<span data-ttu-id="7232e-116">De volgende code laat zien hoe u het totale aantal `QubitClifford`, `T` en `CNOT` poorten die worden gebruikt door een Q #-bewerking kunt ophalen en afdrukken:</span><span class="sxs-lookup"><span data-stu-id="7232e-116">The following code shows how to retrieve and print the total number of `QubitClifford`, `T` and `CNOT` gates used by a Q# operation:</span></span>

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

## <a name="metrics-reported"></a><span data-ttu-id="7232e-117">Gemelde metrische gegevens</span><span class="sxs-lookup"><span data-stu-id="7232e-117">Metrics Reported</span></span>

<span data-ttu-id="7232e-118">Hier volgt een lijst met metrische gegevens die worden geschat door de `ResourcesEstimator`:</span><span class="sxs-lookup"><span data-stu-id="7232e-118">The following is the list of metrics estimated by the `ResourcesEstimator`:</span></span>

* <span data-ttu-id="7232e-119">__CNOT__: het aantal CNOT (ook wel de bewaakte Pauli X Gate)-poorten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7232e-119">__CNOT__: The count of CNOT (also known as the Controlled Pauli X gate) gates executed.</span></span>
* <span data-ttu-id="7232e-120">__QubitClifford__: het aantal uitgevoerde Qubit-Clifford en Pauli-poorten.</span><span class="sxs-lookup"><span data-stu-id="7232e-120">__QubitClifford__: The count of any single qubit Clifford and Pauli gates executed.</span></span>
* <span data-ttu-id="7232e-121">__Meting__: het aantal uitgevoerde metingen.</span><span class="sxs-lookup"><span data-stu-id="7232e-121">__Measure__:  The count of any measurements executed.</span></span>
* <span data-ttu-id="7232e-122">__R__: het aantal Qubit draaiingen dat wordt uitgevoerd, met uitzonde ring van T, Clifford en Pauli-poorten.</span><span class="sxs-lookup"><span data-stu-id="7232e-122">__R__: The count of any single qubit rotations executed, excluding T, Clifford and Pauli gates.</span></span>
* <span data-ttu-id="7232e-123">__T__: het aantal t-poorten en hun bijbehorende conjugaat, inclusief de t-poort, T_x = H. T. H en T_y = hy. t. hy, uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="7232e-123">__T__: The count of T gates and their conjugates, including the T gate, T_x = H.T.H, and T_y = Hy.T.Hy, executed.</span></span>
* <span data-ttu-id="7232e-124">__Diepte__: de diepte van het Quantum circuit dat wordt uitgevoerd door de Q #-bewerking.</span><span class="sxs-lookup"><span data-stu-id="7232e-124">__Depth__: Depth of the quantum circuit executed by the Q# operation.</span></span> <span data-ttu-id="7232e-125">Standaard worden alleen T-poorten in de diepte geteld. Zie de [diepte teller](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7232e-125">By default, only T gates are counted in the depth, see [depth counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) for details.</span></span>
* <span data-ttu-id="7232e-126">__Breedte__: het maximum aantal toegewezen qubits tijdens de uitvoering van de Q #-bewerking.</span><span class="sxs-lookup"><span data-stu-id="7232e-126">__Width__: Maximum number of qubits allocated during the execution of the Q# operation.</span></span>
* <span data-ttu-id="7232e-127">__BorrowedWidth__: het maximum aantal qubits dat is geleend binnen de Q #-bewerking.</span><span class="sxs-lookup"><span data-stu-id="7232e-127">__BorrowedWidth__: Maximum number of qubits borrowed inside the Q# operation.</span></span>


## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="7232e-128">De waarschijnlijkheid van metings resultaten opgeven</span><span class="sxs-lookup"><span data-stu-id="7232e-128">Providing the Probability of Measurement Outcomes</span></span>

<span data-ttu-id="7232e-129"><xref:microsoft.quantum.primitive.assertprob> van de <xref:microsoft.quantum.primitive> naam ruimte kan worden gebruikt om informatie over de verwachte waarschijnlijkheid van een meting te bieden om de uitvoering van het Q #-programma te verhelpen.</span><span class="sxs-lookup"><span data-stu-id="7232e-129"><xref:microsoft.quantum.primitive.assertprob> from the <xref:microsoft.quantum.primitive> namespace can be used to provide information about the expected probability of a measurement to help drive the execution of the Q# program.</span></span> <span data-ttu-id="7232e-130">In het volgende voor beeld ziet u dit:</span><span class="sxs-lookup"><span data-stu-id="7232e-130">The following example illustrates this:</span></span>

```qsharp
operation Teleportation (source : Qubit, target : Qubit) : Unit {

    using (ancilla = Qubit()) {

        H(ancilla);
        CNOT(ancilla, target);

        CNOT(source, ancilla);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [ancilla], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(ancilla) == One) { X(target); X(ancilla); }
    }
}
```

<span data-ttu-id="7232e-131">Wanneer de `ResourcesEstimator` zich voordoet `AssertProb` wordt de meting `PauliZ` op `source` vastgelegd en moet `ancilla` een resultaat van `Zero` met de kans 0,5 worden gegeven.</span><span class="sxs-lookup"><span data-stu-id="7232e-131">When the `ResourcesEstimator` encounters `AssertProb` it will record that measuring `PauliZ` on `source` and `ancilla` should be given an outcome of `Zero` with probability 0.5.</span></span> <span data-ttu-id="7232e-132">Wanneer het `M` later wordt uitgevoerd, worden de vastgelegde waarden van de waarschijnlijkheid van de uitkomst gevonden en `M` wordt `Zero` of `One` geretourneerd met kans 0,5.</span><span class="sxs-lookup"><span data-stu-id="7232e-132">When it executes `M` later, it will find the recorded values of the outcome probabilities and `M` will return `Zero` or `One` with probability 0.5.</span></span>


## <a name="see-also"></a><span data-ttu-id="7232e-133">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7232e-133">See also</span></span>

<span data-ttu-id="7232e-134">De `ResourcesEstimator` is gebouwd op basis van de quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro). Dit biedt een uitgebreidere set metrische gegevens, de mogelijkheid om metrische gegevens te rapporteren over de volledige aanroep-Graph en functies als [afzonderlijke invoer controle](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) om te helpen bij het vinden van fouten in Q #-Program ma's.</span><span class="sxs-lookup"><span data-stu-id="7232e-134">The `ResourcesEstimator` is built on top of the quantum computer [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), which provides a richer set of metrics, the ability to report metrics on the full call-graph, and features like [distinct inputs checker](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) to help find bugs on Q# programs.</span></span> <span data-ttu-id="7232e-135">Raadpleeg de documentatie over de [traceer Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7232e-135">Please refer to the [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) documentation for more information.</span></span>

