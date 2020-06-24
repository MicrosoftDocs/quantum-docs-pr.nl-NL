---
title: Teller voor breedte
description: Meer informatie over de micro soft QDK width Counter, waarmee het aantal qubits wordt geteld dat is toegewezen aan en uitgeleend door elke bewerking in een Quantum programma.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: a76292222950310acc90dded02980e4a5b792e76
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274895"
---
# <a name="width-counter"></a><span data-ttu-id="46dc5-103">Teller voor breedte</span><span class="sxs-lookup"><span data-stu-id="46dc5-103">Width Counter</span></span>

<span data-ttu-id="46dc5-104">Het `Width Counter` telt het aantal qubits dat wordt toegewezen en uitgeleend door elke bewerking.</span><span class="sxs-lookup"><span data-stu-id="46dc5-104">The `Width Counter` counts the number of qubits allocated and borrowed by each operation.</span></span>
<span data-ttu-id="46dc5-105">Alle bewerkingen van de `Microsoft.Quantum.Intrinsic` naam ruimte worden uitgedrukt in termen van één Qubit draaiing, T-Gates, single Qubit Clifford-poorten, CNOT-poorten en metingen van multi-Qubit Pauli observables.</span><span class="sxs-lookup"><span data-stu-id="46dc5-105">All operations from the `Microsoft.Quantum.Intrinsic` namespace are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="46dc5-106">Sommige primitieve bewerkingen kunnen extra qubits toewijzen.</span><span class="sxs-lookup"><span data-stu-id="46dc5-106">Some of the primitive operations can allocate extra qubits.</span></span> <span data-ttu-id="46dc5-107">Bijvoorbeeld gestuurde `X` Gates of gestuurde poorten vermenigvuldigen `T` .</span><span class="sxs-lookup"><span data-stu-id="46dc5-107">For example, multiply controlled `X` gates or controlled `T` gates.</span></span> <span data-ttu-id="46dc5-108">Laat ons het aantal extra qubits berekenen dat is toegewezen door de implementatie van een door een beheerste poort van vermenigvuldiging `X` :</span><span class="sxs-lookup"><span data-stu-id="46dc5-108">Let us compute the number of extra qubits allocated by the implementation of a multiply controlled `X` gate:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a><span data-ttu-id="46dc5-109">De teller width gebruiken binnen een C#-programma</span><span class="sxs-lookup"><span data-stu-id="46dc5-109">Using Width Counter within a C# Program</span></span>

<span data-ttu-id="46dc5-110">Met vermenigvuldiging `X` met een totaal van 5 qubits wordt 2 bijkomende qubits toegewezen en is de invoer breedte 5.</span><span class="sxs-lookup"><span data-stu-id="46dc5-110">Multiply controlled `X` acting on a total of 5 qubits will allocate 2 ancillary qubits and its input width will be 5.</span></span> <span data-ttu-id="46dc5-111">Om te controleren of dit het geval is, kunnen we het volgende C#-programma gebruiken:</span><span class="sxs-lookup"><span data-stu-id="46dc5-111">To check that this is the case, we can use the following C# program:</span></span>

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.useWidthCounter = true;
var sim = new QCTraceSimulator(config);
int totalNumberOfQubits = 5;
var res = ApplyMultiControlledX.Run(sim, totalNumberOfQubits).Result;

double allocatedQubits = 
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.ExtraWidth,
        functor: OperationFunctor.Controlled); 

double inputWidth =
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.InputWidth,
        functor: OperationFunctor.Controlled);
```

<span data-ttu-id="46dc5-112">Het eerste deel van het programma wordt uitgevoerd `ApplyMultiControlledX` .</span><span class="sxs-lookup"><span data-stu-id="46dc5-112">The first part of the program executes `ApplyMultiControlledX`.</span></span> <span data-ttu-id="46dc5-113">In het tweede deel gebruiken we de methode `QCTraceSimulator.GetMetric` om het aantal toegewezen qubits te verkrijgen, evenals het aantal qubits dat is gecontroleerd `X` als invoer.</span><span class="sxs-lookup"><span data-stu-id="46dc5-113">In the second part we use the method `QCTraceSimulator.GetMetric` to get the number of allocated qubits as well as the number of qubits that Controlled `X` received as input.</span></span> 

<span data-ttu-id="46dc5-114">Ten slotte kunnen we het volgende gebruiken om alle statistieken die worden verzameld door de breedte teller in CSV-indeling uit te voeren:</span><span class="sxs-lookup"><span data-stu-id="46dc5-114">Finally, to output all the statistics collected by width counter in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a><span data-ttu-id="46dc5-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="46dc5-115">See also</span></span> ##

- <span data-ttu-id="46dc5-116">Het quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) -overzicht.</span><span class="sxs-lookup"><span data-stu-id="46dc5-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
