---
title: Bronnen Estimator van de Quantum Development Kit
description: 'Meer informatie over de bronnen Estimator, die de resources schat die nodig zijn om een bepaald exemplaar van een Q #-bewerking uit te voeren op een quantum computer.'
author: anpaz-msft
ms.author: anpaz@microsoft.com
ms.date: 1/22/2019
ms.topic: article
uid: microsoft.quantum.machines.resources-estimator
ms.openlocfilehash: b0c800c3946d2e4ba4457127fb9495dc9dcf2934
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274885"
---
# <a name="the-resources-estimator-target-machine"></a><span data-ttu-id="9111b-103">De doel machine van de resources-estimator</span><span class="sxs-lookup"><span data-stu-id="9111b-103">The Resources Estimator Target Machine</span></span>

<span data-ttu-id="9111b-104">Zoals de naam al aangeeft, worden de `ResourcesEstimator` resources die nodig zijn om een bepaald exemplaar van een Q #-bewerking uit te voeren op een quantum computer, geschat.</span><span class="sxs-lookup"><span data-stu-id="9111b-104">As the name implies, the `ResourcesEstimator` estimates the resources required to run a given instance of a Q# operation on a quantum computer.</span></span>
<span data-ttu-id="9111b-105">Dit wordt bereikt door de Quantum bewerking uit te voeren zonder dat de status van een quantum computer werkelijk wordt gesimuleerd. Daarom kunnen er resources worden geschat voor Q #-bewerkingen die gebruikmaken van duizenden qubits als het klassieke deel van de code in een redelijke tijd kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="9111b-105">It accomplishes this by executing the quantum operation without actually simulating the state of a quantum computer; for this reason, it can estimate resources for Q# operations that use thousands of qubits, if the classical part of the code can be run in a reasonable time.</span></span>

## <a name="usage"></a><span data-ttu-id="9111b-106">Gebruik</span><span class="sxs-lookup"><span data-stu-id="9111b-106">Usage</span></span>

<span data-ttu-id="9111b-107">Het `ResourcesEstimator` is slechts een ander type doel computer, zodat het kan worden gebruikt om elke Q #-bewerking uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="9111b-107">The `ResourcesEstimator` is just another type of target machine, thus it can be used to run any Q# operation.</span></span> 

<span data-ttu-id="9111b-108">Als andere doel machines kunt u deze gebruiken voor een C#-hostprogramma een exemplaar maken en dit door geven als de eerste para meter van de methode van de bewerking `Run` :</span><span class="sxs-lookup"><span data-stu-id="9111b-108">As other target machines, to use it on a C# host program create an instance and pass it as the first parameter of the operation's `Run` method:</span></span>

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

<span data-ttu-id="9111b-109">Zoals het voor beeld laat zien, `ResourcesEstimator` biedt het een `ToTSV()` methode om een tabel met door tabs gescheiden waarden (TSV) te genereren die in een bestand kunnen worden opgeslagen of naar de console worden geschreven voor analyse.</span><span class="sxs-lookup"><span data-stu-id="9111b-109">As the example shows, the `ResourcesEstimator` provides a `ToTSV()` method to generate a table with tab-separated-values (TSV) that can be saved into a file or written to the console for analysis.</span></span> <span data-ttu-id="9111b-110">De uitvoer van het bovenstaande programma moet er ongeveer als volgt uitzien:</span><span class="sxs-lookup"><span data-stu-id="9111b-110">The output of the above program should look something like this:</span></span>

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
> <span data-ttu-id="9111b-111">De `ResourcesEstimator` berekeningen worden bij elke uitvoering niet opnieuw ingesteld, als hetzelfde exemplaar wordt gebruikt om een andere bewerking uit te voeren, wordt het samen voegen van het totaal op bestaande resultaten bewaard.</span><span class="sxs-lookup"><span data-stu-id="9111b-111">The `ResourcesEstimator` does not reset its calculations on every run, if the same instance is used to execute another operation it will keep aggregating counts on top of existing results.</span></span>
> <span data-ttu-id="9111b-112">Als u berekeningen tussen uitvoeringen wilt resetten, maakt u voor elke uitvoering een nieuw exemplaar.</span><span class="sxs-lookup"><span data-stu-id="9111b-112">If you need to reset calculations between runs, create a new instance for every execution.</span></span>


## <a name="programmatically-retrieving-the-estimated-data"></a><span data-ttu-id="9111b-113">De geschatte gegevens programmatisch ophalen</span><span class="sxs-lookup"><span data-stu-id="9111b-113">Programmatically Retrieving the Estimated Data</span></span>

<span data-ttu-id="9111b-114">Naast een TSV-tabel kunnen de geschatte bronnen via een programma worden opgehaald via de `ResourcesEstimator` `Data` eigenschap.</span><span class="sxs-lookup"><span data-stu-id="9111b-114">In addition to a TSV table, the resources estimated can be retrieved programmatically via the `ResourcesEstimator`'s `Data` property.</span></span> <span data-ttu-id="9111b-115">`Data`levert een `System.DataTable` exemplaar met twee kolommen: `Metric` en `Sum` , geïndexeerd door de namen van metrische gegevens.</span><span class="sxs-lookup"><span data-stu-id="9111b-115">`Data` provides a `System.DataTable` instance with two columns: `Metric` and `Sum`, indexed by the metrics names.</span></span>

<span data-ttu-id="9111b-116">De volgende code laat zien hoe u het totale aantal `QubitClifford` `T` en de `CNOT` poorten die worden gebruikt door een Q #-bewerking kunt ophalen en afdrukken:</span><span class="sxs-lookup"><span data-stu-id="9111b-116">The following code shows how to retrieve and print the total number of `QubitClifford`, `T` and `CNOT` gates used by a Q# operation:</span></span>

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

## <a name="metrics-reported"></a><span data-ttu-id="9111b-117">Gemelde metrische gegevens</span><span class="sxs-lookup"><span data-stu-id="9111b-117">Metrics Reported</span></span>

<span data-ttu-id="9111b-118">Hier volgt een lijst met metrische gegevens die worden geschat door `ResourcesEstimator` :</span><span class="sxs-lookup"><span data-stu-id="9111b-118">The following is the list of metrics estimated by the `ResourcesEstimator`:</span></span>

* <span data-ttu-id="9111b-119">__CNOT__: het aantal CNOT (ook wel de bewaakte Pauli X Gate)-poorten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="9111b-119">__CNOT__: The count of CNOT (also known as the Controlled Pauli X gate) gates executed.</span></span>
* <span data-ttu-id="9111b-120">__QubitClifford__: het aantal uitgevoerde Qubit-Clifford en Pauli-poorten.</span><span class="sxs-lookup"><span data-stu-id="9111b-120">__QubitClifford__: The count of any single qubit Clifford and Pauli gates executed.</span></span>
* <span data-ttu-id="9111b-121">__Meting__: het aantal uitgevoerde metingen.</span><span class="sxs-lookup"><span data-stu-id="9111b-121">__Measure__:  The count of any measurements executed.</span></span>
* <span data-ttu-id="9111b-122">__R__: het aantal Qubit draaiingen dat wordt uitgevoerd, met uitzonde ring van T, Clifford en Pauli-poorten.</span><span class="sxs-lookup"><span data-stu-id="9111b-122">__R__: The count of any single qubit rotations executed, excluding T, Clifford and Pauli gates.</span></span>
* <span data-ttu-id="9111b-123">__T__: het aantal t-poorten en hun bijbehorende conjugaat, inclusief de t-poort, T_x = H. t. H en T_y = hy. t. hy, uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="9111b-123">__T__: The count of T gates and their conjugates, including the T gate, T_x = H.T.H, and T_y = Hy.T.Hy, executed.</span></span>
* <span data-ttu-id="9111b-124">__Diepte__: de diepte van het Quantum circuit dat wordt uitgevoerd door de Q #-bewerking.</span><span class="sxs-lookup"><span data-stu-id="9111b-124">__Depth__: Depth of the quantum circuit executed by the Q# operation.</span></span> <span data-ttu-id="9111b-125">Standaard worden alleen T-poorten in de diepte geteld. Zie de [diepte teller](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="9111b-125">By default, only T gates are counted in the depth, see [depth counter](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter) for details.</span></span>
* <span data-ttu-id="9111b-126">__Breedte__: het maximum aantal toegewezen qubits tijdens de uitvoering van de Q #-bewerking.</span><span class="sxs-lookup"><span data-stu-id="9111b-126">__Width__: Maximum number of qubits allocated during the execution of the Q# operation.</span></span>
* <span data-ttu-id="9111b-127">__BorrowedWidth__: het maximum aantal qubits dat is geleend binnen de Q #-bewerking.</span><span class="sxs-lookup"><span data-stu-id="9111b-127">__BorrowedWidth__: Maximum number of qubits borrowed inside the Q# operation.</span></span>


## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="9111b-128">De waarschijnlijkheid van metingsresultaten opgeven</span><span class="sxs-lookup"><span data-stu-id="9111b-128">Providing the Probability of Measurement Outcomes</span></span>

<span data-ttu-id="9111b-129"><xref:microsoft.quantum.intrinsic.assertprob>vanuit de <xref:microsoft.quantum.intrinsic> naam ruimte kan worden gebruikt om informatie over de verwachte waarschijnlijkheid van een meting te bieden om de uitvoering van het Q #-programma te verhelpen.</span><span class="sxs-lookup"><span data-stu-id="9111b-129"><xref:microsoft.quantum.intrinsic.assertprob> from the <xref:microsoft.quantum.intrinsic> namespace can be used to provide information about the expected probability of a measurement to help drive the execution of the Q# program.</span></span> <span data-ttu-id="9111b-130">Het volgende voorbeeld illustreert dit:</span><span class="sxs-lookup"><span data-stu-id="9111b-130">The following example illustrates this:</span></span>

```qsharp
operation Teleport(source : Qubit, target : Qubit) : Unit {

    using (qubit = Qubit()) {

        H(q);
        CNOT(qubit, target);

        CNOT(source, qubit);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [qubit], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(qubit) == One) { X(target); X(qubit); }
    }
}
```

<span data-ttu-id="9111b-131">Als er `ResourcesEstimator` wordt gestuit `AssertProb` , wordt dat meet tijdstip vastgelegd `PauliZ` `source` en `q` moet er een resultaat worden gegeven van de `Zero` kans 0,5.</span><span class="sxs-lookup"><span data-stu-id="9111b-131">When the `ResourcesEstimator` encounters `AssertProb` it will record that measuring `PauliZ` on `source` and `q` should be given an outcome of `Zero` with probability 0.5.</span></span> <span data-ttu-id="9111b-132">Wanneer het later wordt uitgevoerd `M` , worden de vastgelegde waarden van de resultaten kansen gevonden en `M` geretourneerd, `Zero` of `One` met kans van 0,5.</span><span class="sxs-lookup"><span data-stu-id="9111b-132">When it executes `M` later, it will find the recorded values of the outcome probabilities and `M` will return `Zero` or `One` with probability 0.5.</span></span>


## <a name="see-also"></a><span data-ttu-id="9111b-133">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9111b-133">See also</span></span>

<span data-ttu-id="9111b-134">De `ResourcesEstimator` is gebouwd op basis van de quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), met een uitgebreidere set metrische gegevens, de mogelijkheid om metrische gegevens te rapporteren over de volledige aanroep-Graph en functies als [afzonderlijke invoer controle](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) om te helpen bij het vinden van fouten in Q #-Program ma's.</span><span class="sxs-lookup"><span data-stu-id="9111b-134">The `ResourcesEstimator` is built on top of the quantum computer [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro), which provides a richer set of metrics, the ability to report metrics on the full call-graph, and features like [distinct inputs checker](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs) to help find bugs on Q# programs.</span></span> <span data-ttu-id="9111b-135">Raadpleeg de documentatie over de [traceer Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="9111b-135">Please refer to the [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) documentation for more information.</span></span>

