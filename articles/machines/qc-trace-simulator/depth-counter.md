---
title: Diepte teller
description: Meer informatie over het micro soft QDK depth Counter, waarmee u het aantal niveaus van elke bewerking die wordt aangeroepen in een Quantum programma, kunt verzamelen.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: d532a9f512b8c87d83d62ed26e3bb67e1b6f668b
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906097"
---
# <a name="depth-counter"></a><span data-ttu-id="b489b-103">Diepte teller</span><span class="sxs-lookup"><span data-stu-id="b489b-103">Depth Counter</span></span>

<span data-ttu-id="b489b-104">De `Depth Counter` maakt deel uit van de quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span><span class="sxs-lookup"><span data-stu-id="b489b-104">The `Depth Counter` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span>
<span data-ttu-id="b489b-105">Het wordt gebruikt om aantallen te verzamelen van de diepte van elke bewerking die wordt aangeroepen in een Quantum programma.</span><span class="sxs-lookup"><span data-stu-id="b489b-105">It is used to gather counts of the depth of every operation invoked in a quantum program.</span></span> <span data-ttu-id="b489b-106">Alle bewerkingen van <xref:microsoft.quantum.intrinsic> worden uitgedrukt in termen van één Qubit rotatie, T-poorten, enkelvoudige Qubit Clifford-poorten, CNOT poorten en metingen van multi-Qubit Pauli observables.</span><span class="sxs-lookup"><span data-stu-id="b489b-106">All operations from <xref:microsoft.quantum.intrinsic> are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="b489b-107">Gebruikers kunnen de diepte instellen voor elk van de primitieve bewerkingen via het `gateTimes` veld van <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.</span><span class="sxs-lookup"><span data-stu-id="b489b-107">Users can set the depth for each of the primitive operations via the `gateTimes` field of <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.</span></span>

<span data-ttu-id="b489b-108">Standaard hebben alle bewerkingen diepte 0, met uitzonde ring van de T-poort, die diepte 1 heeft.</span><span class="sxs-lookup"><span data-stu-id="b489b-108">By default, all operations have depth 0 except the T gate which has depth 1.</span></span> <span data-ttu-id="b489b-109">Dit betekent dat standaard alleen de w-diepte van bewerkingen wordt berekend (vaak gewenst).</span><span class="sxs-lookup"><span data-stu-id="b489b-109">This means that by default, only the T depth of operations is computed (which is often desirable).</span></span> <span data-ttu-id="b489b-110">Verzamelde statistieken worden geaggregeerd over alle randen van de operations call-grafiek.</span><span class="sxs-lookup"><span data-stu-id="b489b-110">Collected statistics are aggregated over all the edges of the operations call graph.</span></span> 

<span data-ttu-id="b489b-111">Laat ons nu de <xref:microsoft.quantum.intrinsic.t> diepte van de <xref:microsoft.quantum.intrinsic.ccnot> bewerking berekenen.</span><span class="sxs-lookup"><span data-stu-id="b489b-111">Let us now compute the <xref:microsoft.quantum.intrinsic.t> depth of the <xref:microsoft.quantum.intrinsic.ccnot> operation.</span></span> <span data-ttu-id="b489b-112">We zullen de volgende Q #-voorbeeld code gebruiken:</span><span class="sxs-lookup"><span data-stu-id="b489b-112">We will use the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

## <a name="using-depth-counter-within-a-c-program"></a><span data-ttu-id="b489b-113">Diepte teller in een C# programma gebruiken</span><span class="sxs-lookup"><span data-stu-id="b489b-113">Using Depth Counter within a C# Program</span></span>

<span data-ttu-id="b489b-114">Ga als volgt te werk om te controleren of `CCNOT` `T` diepte 5 heeft en `ApplySampleWithCCNOT` `T` diepte 6 C# hebben, dan kunnen we de volgende code gebruiken:</span><span class="sxs-lookup"><span data-stu-id="b489b-114">To check that `CCNOT` has `T` depth 5 and `ApplySampleWithCCNOT` has `T` depth 6 we can use the following C# code:</span></span>

```csharp
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.useDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="b489b-115">Het eerste deel van het programma voert `ApplySampleWithCCNOT`uit.</span><span class="sxs-lookup"><span data-stu-id="b489b-115">The first part of the program executes `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="b489b-116">In het tweede deel gebruiken we de methode `QCTraceSimulator.GetMetric` om de `T` diepte van `CCNOT` en `ApplySampleWithCCNOT`te verkrijgen:</span><span class="sxs-lookup"><span data-stu-id="b489b-116">In the second part, we use the method `QCTraceSimulator.GetMetric` to get the `T` depth of `CCNOT` and `ApplySampleWithCCNOT`:</span></span> 

```csharp
double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="b489b-117">Ten slotte kunnen we het volgende gebruiken voor het uitvoeren van alle statistieken die worden verzameld door `Depth Counter` in CSV-indeling:</span><span class="sxs-lookup"><span data-stu-id="b489b-117">Finally, to output all the statistics collected by `Depth Counter` in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a><span data-ttu-id="b489b-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b489b-118">See also</span></span> ##

- <span data-ttu-id="b489b-119">Het quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) -overzicht.</span><span class="sxs-lookup"><span data-stu-id="b489b-119">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
