---
title: Primitieve bewerkingen teller | Quantum computer Trace Simulator | Microsoft Docs
description: Overzicht van kwantumcomputer-traceersimulator
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
ms.openlocfilehash: 1f554c0a1b92c8f6b59be3a9d9965e0e25bd074f
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820416"
---
# <a name="primitive-operations-counter"></a><span data-ttu-id="d2f3e-103">Teller voor primitieve bewerkingen</span><span class="sxs-lookup"><span data-stu-id="d2f3e-103">Primitive Operations Counter</span></span>  

<span data-ttu-id="d2f3e-104">De `Primitive Operations Counter` maakt deel uit van de quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span><span class="sxs-lookup"><span data-stu-id="d2f3e-104">The `Primitive Operations Counter` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="d2f3e-105">Het telt het aantal primitieve uitvoeringen dat wordt gebruikt door elke bewerking die wordt aangeroepen in een Quantum programma.</span><span class="sxs-lookup"><span data-stu-id="d2f3e-105">It counts the number of primitive executions used by every operation invoked in a quantum program.</span></span> <span data-ttu-id="d2f3e-106">Alle bewerkingen van `Microsoft.Quantum.Intrinsic` worden uitgedrukt in termen van één Qubit rotatie, T-poorten, enkelvoudige Qubit Clifford-poorten, CNOT poorten en metingen van multi-Qubit Pauli observables.</span><span class="sxs-lookup"><span data-stu-id="d2f3e-106">All operations from `Microsoft.Quantum.Intrinsic` are expressed in terms of single qubit rotations, T gates, single qubit Clifford gates, CNOT gates and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="d2f3e-107">Verzamelde statistieken worden geaggregeerd over de randen van de operations call-grafiek.</span><span class="sxs-lookup"><span data-stu-id="d2f3e-107">Collected statistics are aggregated over the edges of the operations call graph.</span></span> <span data-ttu-id="d2f3e-108">We tellen nu hoeveel `T` Gates nodig zijn voor het implementeren van de `CCNOT` bewerking.</span><span class="sxs-lookup"><span data-stu-id="d2f3e-108">Let us now count how many `T` gates are needed to implement the `CCNOT` operation.</span></span> 

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    } 
}
```

## <a name="using-the-primitive-operations-counter-within-a-c-program"></a><span data-ttu-id="d2f3e-109">Het item primitieve bewerkingen in een C# programma gebruiken</span><span class="sxs-lookup"><span data-stu-id="d2f3e-109">Using the Primitive Operations Counter within a C# Program</span></span>

<span data-ttu-id="d2f3e-110">Ga als volgt te werk om te controleren of `CCNOT` enige 7 `T` poorten vereist en dat `ApplySampleWithCCNOT` acht `T` poorten worden C# uitgevoerd, kunnen we de volgende code gebruiken:</span><span class="sxs-lookup"><span data-stu-id="d2f3e-110">To check that `CCNOT` indeed requires 7 `T` gates and that `ApplySampleWithCCNOT` executes 8 `T` gates we can use the following C# code:</span></span>

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.usePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="d2f3e-111">Het eerste deel van het programma voert `ApplySampleWithCCNOT`uit.</span><span class="sxs-lookup"><span data-stu-id="d2f3e-111">The first part of the program executes `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="d2f3e-112">In het tweede deel gebruiken we de methode `QCTraceSimulator.GetMetric` om het aantal T-poorten te verkrijgen dat door `ApplySampleWithCCNOT`wordt uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="d2f3e-112">In the second part, we use the method `QCTraceSimulator.GetMetric` to get the number of T gates executed by `ApplySampleWithCCNOT`:</span></span> 

```csharp
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="d2f3e-113">Als `GetMetric` wordt aangeroepen met twee type parameters, wordt de waarde van de metriek geretourneerd die is gekoppeld aan een bepaalde rand van de oproep grafiek.</span><span class="sxs-lookup"><span data-stu-id="d2f3e-113">When `GetMetric` is called with two type parameters it returns the value of the metric associated with a given call graph edge.</span></span> <span data-ttu-id="d2f3e-114">In de voorbeeld bewerking `Primitive.CCNOT` wordt aangeroepen in `ApplySampleWithCCNOT`, waardoor de oproep grafiek de rand `<Primitive.CCNOT, ApplySampleWithCCNOT>`bevat.</span><span class="sxs-lookup"><span data-stu-id="d2f3e-114">In our example operation `Primitive.CCNOT` is called within `ApplySampleWithCCNOT` and therefore the call graph contains the edge `<Primitive.CCNOT, ApplySampleWithCCNOT>`.</span></span> 

<span data-ttu-id="d2f3e-115">Om het aantal `CNOT` gebruikte poorten te verkrijgen, kunnen we de volgende regel toevoegen:</span><span class="sxs-lookup"><span data-stu-id="d2f3e-115">To get the number of `CNOT` gates used, we can add the following line:</span></span>
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

<span data-ttu-id="d2f3e-116">Ten slotte kunnen we het volgende gebruiken voor het uitvoeren van alle statistieken die worden verzameld door de poort teller in CSV-indeling:</span><span class="sxs-lookup"><span data-stu-id="d2f3e-116">Finally, to output all the statistics collected by the gate counter in CSV format we can use the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a><span data-ttu-id="d2f3e-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d2f3e-117">See also</span></span> ##

- <span data-ttu-id="d2f3e-118">Het quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) -overzicht.</span><span class="sxs-lookup"><span data-stu-id="d2f3e-118">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
