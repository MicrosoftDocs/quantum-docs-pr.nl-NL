---
title: Diepte teller-Quantum Development Kit
description: Meer informatie over het micro soft QDK depth Counter, dat gebruikmaakt van de Quantum Trace Simulator om aantallen te verzamelen van de diepte van elke bewerking die wordt aangeroepen in een Q# programma.
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: 9c3a772861582e5c49fe5ad27519c25a59d617b1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98859049"
---
# <a name="quantum-trace-simulator-depth-counter"></a>Quantum Trace Simulator: Depth Counter

De teller depth is onderdeel van de Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).
U kunt deze gebruiken om aantallen te verzamelen die de ondergrens vertegenwoordigen van elke bewerking die wordt aangeroepen in een Quantum programma. 

## <a name="depth-values"></a>Diepte waarden

Standaard hebben alle bewerkingen een diepte van **0** , met uitzonde ring van de `T` bewerking, die een diepte van **1** heeft. Dit betekent dat standaard alleen de `T` diepte van bewerkingen wordt berekend (vaak gewenst). Met de diepte teller worden statistieken geaggregeerd en verzameld over alle randen van de [aanroep grafiek](https://en.wikipedia.org/wiki/Call_graph)van de bewerking.

Alle <xref:Microsoft.Quantum.Intrinsic> bewerkingen worden uitgedrukt in termen van Qubit draaiingen, <xref:Microsoft.Quantum.Intrinsic.T> bewerkingen, single-Qubit Clifford-bewerkingen, <xref:Microsoft.Quantum.Intrinsic.CNOT> bewerkingen en metingen van multi-Qubit Pauli observables. Gebruikers kunnen de diepte instellen voor elk van de primitieve bewerkingen via het `gateTimes` veld van <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .

## <a name="invoking-the-depth-counter"></a>Aanroepen van diepte teller

Als u de Quantum Trace Simulator wilt uitvoeren met het teller depth, moet u een <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> exemplaar maken, de `UseDepthCounter` eigenschap instellen op **True** en vervolgens een nieuw <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> exemplaar maken met `QCTraceSimulatorConfiguration` als de para meter. 

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

`CCNOT` `T`  `ApplySampleWithCCNOT` `T` Gebruik de volgende C#-code om te controleren of deze diepte 5 en diepte 6 heeft:

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

## <a name="see-also"></a>Zie ook

- Het Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Overview (Engelstalig).
- De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-verwijzing.
- De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-verwijzing.
- De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.DepthCounter> API-verwijzing.
