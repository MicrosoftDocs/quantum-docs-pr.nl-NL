---
title: Diepte teller-Quantum Development Kit
description: 'Meer informatie over het micro soft QDK depth Counter, dat gebruikmaakt van de Quantum Trace Simulator om aantallen te verzamelen van de diepte van elke bewerking die wordt aangeroepen in een Q #-programma.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: 811e387fedf547d2681518ae0bb525c13dc84ff4
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871124"
---
# <a name="quantum-trace-simulator-depth-counter"></a><span data-ttu-id="5d071-103">Quantum Trace Simulator: Depth Counter</span><span class="sxs-lookup"><span data-stu-id="5d071-103">Quantum trace simulator: depth counter</span></span>

<span data-ttu-id="5d071-104">De teller depth is onderdeel van de Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span><span class="sxs-lookup"><span data-stu-id="5d071-104">The depth counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span>
<span data-ttu-id="5d071-105">U kunt deze gebruiken om aantallen te verzamelen die de ondergrens vertegenwoordigen van elke bewerking die wordt aangeroepen in een Quantum programma.</span><span class="sxs-lookup"><span data-stu-id="5d071-105">You can use it to gather counts that represent the lower bound of the depth of every operation invoked in a quantum program.</span></span> 

## <a name="depth-values"></a><span data-ttu-id="5d071-106">Diepte waarden</span><span class="sxs-lookup"><span data-stu-id="5d071-106">Depth values</span></span>

<span data-ttu-id="5d071-107">Standaard hebben alle bewerkingen een diepte van **0** , met uitzonde ring van de `T` bewerking, die een diepte van **1**heeft.</span><span class="sxs-lookup"><span data-stu-id="5d071-107">By default, all operations have a depth of **0** except the `T` operation, which has a depth of **1**.</span></span> <span data-ttu-id="5d071-108">Dit betekent dat standaard alleen de `T` diepte van bewerkingen wordt berekend (vaak gewenst).</span><span class="sxs-lookup"><span data-stu-id="5d071-108">This means that by default, only the `T` depth of operations is computed (which is often desirable).</span></span> <span data-ttu-id="5d071-109">Met de diepte teller worden statistieken geaggregeerd en verzameld over alle randen van de [aanroep grafiek](https://en.wikipedia.org/wiki/Call_graph)van de bewerking.</span><span class="sxs-lookup"><span data-stu-id="5d071-109">The depth counter aggregates and collects statistics over all the edges of the operation's [call graph](https://en.wikipedia.org/wiki/Call_graph).</span></span>

<span data-ttu-id="5d071-110">Alle <xref:microsoft.quantum.intrinsic> bewerkingen worden uitgedrukt in termen van Qubit draaiingen, <xref:microsoft.quantum.intrinsic.t> bewerkingen, single-Qubit Clifford-bewerkingen, <xref:microsoft.quantum.intrinsic.cnot> bewerkingen en metingen van multi-Qubit Pauli observables.</span><span class="sxs-lookup"><span data-stu-id="5d071-110">All <xref:microsoft.quantum.intrinsic> operations are expressed in terms of single-qubit rotations, <xref:microsoft.quantum.intrinsic.t> operations, single-qubit Clifford operations, <xref:microsoft.quantum.intrinsic.cnot> operations, and measurements of multi-qubit Pauli observables.</span></span> <span data-ttu-id="5d071-111">Gebruikers kunnen de diepte instellen voor elk van de primitieve bewerkingen via het `gateTimes` veld van <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .</span><span class="sxs-lookup"><span data-stu-id="5d071-111">Users can set the depth for each of the primitive operations via the `gateTimes` field of <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.</span></span>

## <a name="invoking-the-depth-counter"></a><span data-ttu-id="5d071-112">Aanroepen van diepte teller</span><span class="sxs-lookup"><span data-stu-id="5d071-112">Invoking the depth counter</span></span>

<span data-ttu-id="5d071-113">Als u de Quantum Trace Simulator wilt uitvoeren met het teller depth, moet u een <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> exemplaar maken, de `UseDepthCounter` eigenschap instellen op **True**en vervolgens een nieuw <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> exemplaar maken met `QCTraceSimulatorConfiguration` als de para meter.</span><span class="sxs-lookup"><span data-stu-id="5d071-113">To run the quantum trace simulator with the depth counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set its `UseDepthCounter` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-depth-counter-in-a-c-host-program"></a><span data-ttu-id="5d071-114">Het item depth gebruiken in een C#-hostprogramma</span><span class="sxs-lookup"><span data-stu-id="5d071-114">Using the depth counter in a C# host program</span></span>

<span data-ttu-id="5d071-115">In het C#-voor beeld dat volgt in deze sectie `T` wordt de diepte van de `CCNOT` bewerking berekend op basis van de volgende Q #-voorbeeld code:</span><span class="sxs-lookup"><span data-stu-id="5d071-115">The C# example that follows in this section computes the `T` depth of the `CCNOT` operation, based on the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

<span data-ttu-id="5d071-116">`CCNOT` `T` **5** `ApplySampleWithCCNOT` `T` Gebruik de volgende C#-code om te controleren **6**of deze diepte 5 en diepte 6 heeft:</span><span class="sxs-lookup"><span data-stu-id="5d071-116">To check that `CCNOT` has `T` depth **5** and `ApplySampleWithCCNOT` has `T` depth **6**, use the following C# code:</span></span>

```csharp
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

<span data-ttu-id="5d071-117">Het eerste deel van het programma wordt uitgevoerd `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="5d071-117">The first part of the program runs `ApplySampleWithCCNOT`.</span></span> <span data-ttu-id="5d071-118">Het tweede deel maakt gebruik [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) van de methode voor het ophalen `T` van de diepte van `CCNOT` en `ApplySampleWithCCNOT` .</span><span class="sxs-lookup"><span data-stu-id="5d071-118">The second part uses the [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the `T` depth of `CCNOT` and `ApplySampleWithCCNOT`.</span></span> 

<span data-ttu-id="5d071-119">Ten slotte kunt u alle statistieken die worden verzameld door de teller depth in CSV-indeling uitvoeren met het volgende:</span><span class="sxs-lookup"><span data-stu-id="5d071-119">Finally, you can output all the statistics collected by the depth counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a><span data-ttu-id="5d071-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5d071-120">See also</span></span>

- <span data-ttu-id="5d071-121">Het Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Overview (Engelstalig).</span><span class="sxs-lookup"><span data-stu-id="5d071-121">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="5d071-122">De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-verwijzing.</span><span class="sxs-lookup"><span data-stu-id="5d071-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="5d071-123">De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-verwijzing.</span><span class="sxs-lookup"><span data-stu-id="5d071-123">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="5d071-124">De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter> API-verwijzing.</span><span class="sxs-lookup"><span data-stu-id="5d071-124">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter> API reference.</span></span>
