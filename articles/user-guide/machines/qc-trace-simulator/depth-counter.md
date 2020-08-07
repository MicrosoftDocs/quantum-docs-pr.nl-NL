---
title: Diepte teller-Quantum Development Kit
description: Meer informatie over het micro soft QDK depth Counter, dat gebruikmaakt van de Quantum Trace Simulator om aantallen te verzamelen van de diepte van elke bewerking die wordt aangeroepen in een Q# programma.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: 5c54f6fc479203d30c68c4958329605d4323f9ea
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868318"
---
# <a name="quantum-trace-simulator-depth-counter"></a>Quantum Trace Simulator: Depth Counter

De teller depth is onderdeel van de Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).
U kunt deze gebruiken om aantallen te verzamelen die de ondergrens vertegenwoordigen van elke bewerking die wordt aangeroepen in een Quantum programma. 

## <a name="depth-values"></a>Diepte waarden

Standaard hebben alle bewerkingen een diepte van **0** , met uitzonde ring van de `T` bewerking, die een diepte van **1**heeft. Dit betekent dat standaard alleen de `T` diepte van bewerkingen wordt berekend (vaak gewenst). Met de diepte teller worden statistieken geaggregeerd en verzameld over alle randen van de [aanroep grafiek](https://en.wikipedia.org/wiki/Call_graph)van de bewerking.

Alle <xref:microsoft.quantum.intrinsic> bewerkingen worden uitgedrukt in termen van Qubit draaiingen, <xref:microsoft.quantum.intrinsic.t> bewerkingen, single-Qubit Clifford-bewerkingen, <xref:microsoft.quantum.intrinsic.cnot> bewerkingen en metingen van multi-Qubit Pauli observables. Gebruikers kunnen de diepte instellen voor elk van de primitieve bewerkingen via het `gateTimes` veld van <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .

## <a name="invoking-the-depth-counter"></a>Aanroepen van diepte teller

Als u de Quantum Trace Simulator wilt uitvoeren met het teller depth, moet u een <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> exemplaar maken, de `UseDepthCounter` eigenschap instellen op **True**en vervolgens een nieuw <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> exemplaar maken met `QCTraceSimulatorConfiguration` als de para meter. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDepthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-depth-counter-in-a-c-host-program"></a>Het item depth gebruiken in een C#-hostprogramma

In het C#-voor beeld dat volgt in deze sectie `T` wordt de diepte van de `CCNOT` bewerking berekend op basis van de volgende Q# voorbeeld code:

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

`CCNOT` `T` **5** `ApplySampleWithCCNOT` `T` Gebruik de volgende C#-code om te controleren **6**of deze diepte 5 en diepte 6 heeft:

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

Het eerste deel van het programma wordt uitgevoerd `ApplySampleWithCCNOT` . Het tweede deel maakt gebruik [`GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) van de methode voor het ophalen `T` van de diepte van `CCNOT` en `ApplySampleWithCCNOT` . 

Ten slotte kunt u alle statistieken die worden verzameld door de teller depth in CSV-indeling uitvoeren met het volgende:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a>Zie tevens

- Het Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Overview (Engelstalig).
- De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-verwijzing.
- De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-verwijzing.
- De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter> API-verwijzing.
