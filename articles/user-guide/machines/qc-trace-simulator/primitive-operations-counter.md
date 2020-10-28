---
title: Teller voor primitieve bewerkingen-Quantum Development Kit
description: 'Meer informatie over het micro soft QDK primitieve bewerkings item, dat gebruikmaakt van de Quantum Trace Simulator om primitieve processen bij te houden die worden gebruikt door bewerkingen in een :::no-loc(Q#)::: programma.'
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: bf75eb94696a489a587316928bc3f33baa4a1785
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92690955"
---
# <a name="quantum-trace-simulator-primitive-operations-counter"></a><span data-ttu-id="03a45-103">Quantum Trace Simulator: primitieve bewerkingen teller</span><span class="sxs-lookup"><span data-stu-id="03a45-103">Quantum trace simulator: primitive operations counter</span></span>

<span data-ttu-id="03a45-104">Het teller primitieve bewerking maakt deel uit van de Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span><span class="sxs-lookup"><span data-stu-id="03a45-104">The primitive operation counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="03a45-105">Hiermee wordt het aantal primitieve processen geteld dat wordt gebruikt door elke bewerking die wordt aangeroepen in een Quantum programma.</span><span class="sxs-lookup"><span data-stu-id="03a45-105">It counts the number of primitive processes used by every operation invoked in a quantum program.</span></span> 

<span data-ttu-id="03a45-106">Alle <xref:Microsoft.Quantum.Intrinsic> bewerkingen worden uitgedrukt in termen van Qubit draaiingen, T-bewerkingen, single-Qubit Clifford-bewerkingen, CNOT bewerkingen en metingen van multi-Qubit Pauli observables.</span><span class="sxs-lookup"><span data-stu-id="03a45-106">All <xref:Microsoft.Quantum.Intrinsic> operations are expressed in terms of single-qubit rotations, T operations, single-qubit Clifford operations, CNOT operations, and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="03a45-107">Met het teller primitieve bewerkingen worden statistieken geaggregeerd en verzameld over alle randen van de [aanroep grafiek](https://en.wikipedia.org/wiki/Call_graph)van de bewerking.</span><span class="sxs-lookup"><span data-stu-id="03a45-107">The Primitive Operations Counter aggregates and collects statistics over all the edges of the operation's [call graph](https://en.wikipedia.org/wiki/Call_graph).</span></span>

## <a name="invoking-the-primitive-operation-counter"></a><span data-ttu-id="03a45-108">Het item primitieve bewerking aanroepen</span><span class="sxs-lookup"><span data-stu-id="03a45-108">Invoking the primitive operation counter</span></span>

<span data-ttu-id="03a45-109">Als u de Quantum Trace Simulator wilt uitvoeren met het teller primitieve bewerking, moet u een <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> exemplaar maken, de `UsePrimitiveOperationsCounter` eigenschap instellen op **waar** en vervolgens een nieuw <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> exemplaar maken met de `QCTraceSimulatorConfiguration` as-para meter.</span><span class="sxs-lookup"><span data-stu-id="03a45-109">To run the quantum trace simulator with the primitive operation counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UsePrimitiveOperationsCounter` property to **true** , and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with the `QCTraceSimulatorConfiguration` as the parameter.</span></span>

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-primitive-operation-counter-in-a-c-host-program"></a><span data-ttu-id="03a45-110">Het teller primitieve bewerking in een C#-hostprogramma gebruiken</span><span class="sxs-lookup"><span data-stu-id="03a45-110">Using the primitive operation counter in a C# host program</span></span>

<span data-ttu-id="03a45-111">Het C#-voor beeld dat volgt in deze sectie telt het aantal <xref:Microsoft.Quantum.Intrinsic.T> bewerkingen dat nodig is voor het implementeren van de <xref:Microsoft.Quantum.Intrinsic.ccnot> bewerking, op basis van de volgende :::no-loc(Q#)::: voorbeeld code:</span><span class="sxs-lookup"><span data-stu-id="03a45-111">The C# example that follows in this section counts how many <xref:Microsoft.Quantum.Intrinsic.T> operations are needed to implement the <xref:Microsoft.Quantum.Intrinsic.ccnot> operation, based on the following :::no-loc(Q#)::: sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

<span data-ttu-id="03a45-112">`CCNOT` `T` `ApplySampleWithCCNOT` `T` Gebruik de volgende C#-code om te controleren dat zeven bewerkingen vereist en acht bewerkingen uitvoert:</span><span class="sxs-lookup"><span data-stu-id="03a45-112">To check that `CCNOT` requires seven `T` operations and that `ApplySampleWithCCNOT` runs eight `T` operations, use the following C# code:</span></span>

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

<span data-ttu-id="03a45-113">Het eerste deel van het programma wordt uitgevoerd `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="03a45-113">The first part of the program runs `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="03a45-114">In het tweede deel wordt gebruikgemaakt [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) van de methode voor het ophalen van het aantal bewerkingen dat wordt `T` uitgevoerd door `ApplySampleWithCCNOT` :</span><span class="sxs-lookup"><span data-stu-id="03a45-114">The second part uses the [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the number of `T` operations run by `ApplySampleWithCCNOT`:</span></span> 

<span data-ttu-id="03a45-115">Wanneer u `GetMetric` met twee type parameters aanroept, wordt de waarde van de metriek geretourneerd die is gekoppeld aan een bepaalde rand van de oproep grafiek.</span><span class="sxs-lookup"><span data-stu-id="03a45-115">When you call `GetMetric` with two type parameters, it returns the value of the metric associated with a given call graph edge.</span></span> <span data-ttu-id="03a45-116">In het voor gaande voor beeld roept het programma de `Primitive.CCNOT` bewerking binnen `ApplySampleWithCCNOT` en daarom bevat de oproep grafiek de rand `<Primitive.CCNOT, ApplySampleWithCCNOT>` .</span><span class="sxs-lookup"><span data-stu-id="03a45-116">In the preceding example, the program calls the `Primitive.CCNOT` operation  within `ApplySampleWithCCNOT` and therefore the call graph contains the edge `<Primitive.CCNOT, ApplySampleWithCCNOT>`.</span></span> 

<span data-ttu-id="03a45-117">`CNOT`Voeg de volgende regel toe om het aantal gebruikte bewerkingen op te halen:</span><span class="sxs-lookup"><span data-stu-id="03a45-117">To retrieve the number of `CNOT` operations used, add the following line:</span></span>
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

<span data-ttu-id="03a45-118">Ten slotte kunt u alle statistieken die door het item primitieve bewerkingen zijn verzameld, in CSV-indeling uitvoeren met het volgende:</span><span class="sxs-lookup"><span data-stu-id="03a45-118">Finally, you can output all the statistics collected by the Primitive Operations Counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a><span data-ttu-id="03a45-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="03a45-119">See also</span></span>

- <span data-ttu-id="03a45-120">Het Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Overview (Engelstalig).</span><span class="sxs-lookup"><span data-stu-id="03a45-120">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="03a45-121">De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-verwijzing.</span><span class="sxs-lookup"><span data-stu-id="03a45-121">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="03a45-122">De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-verwijzing.</span><span class="sxs-lookup"><span data-stu-id="03a45-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="03a45-123">De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames> API-verwijzing.</span><span class="sxs-lookup"><span data-stu-id="03a45-123">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames> API reference.</span></span>