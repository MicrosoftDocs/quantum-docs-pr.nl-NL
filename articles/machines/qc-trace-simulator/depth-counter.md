---
title: Diepte teller | Quantum computer Trace Simulator | Microsoft Docs
description: Overzicht van quantum computer Trace Simulator
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: f5fcaa64e91290d377eeba597df2e307e187277c
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184896"
---
# <a name="depth-counter"></a>Diepte teller

De `Depth Counter` maakt deel uit van de quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).
Het wordt gebruikt om aantallen te verzamelen van de diepte van elke bewerking die wordt aangeroepen in een Quantum programma. Alle bewerkingen van <xref:microsoft.quantum.intrinsic> worden uitgedrukt in termen van één Qubit rotatie, T-poorten, enkelvoudige Qubit Clifford-poorten, CNOT poorten en metingen van multi-Qubit Pauli observables. Gebruikers kunnen de diepte instellen voor elk van de primitieve bewerkingen via het `gateTimes` veld van <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration>.

Standaard hebben alle bewerkingen diepte 0, met uitzonde ring van de T-poort, die diepte 1 heeft. Dit betekent dat standaard alleen de w-diepte van bewerkingen wordt berekend (vaak gewenst). Verzamelde statistieken worden geaggregeerd over alle randen van de operations call-grafiek. 

Laat ons nu de <xref:microsoft.quantum.intrinsic.t> diepte van de <xref:microsoft.quantum.intrinsic.ccnot> bewerking berekenen. We gebruiken de volgende Q #-Stuur code: 

```qsharp
open Microsoft.Quantum.Primitive;
operation CCNOTDriver() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

## <a name="using-depth-counter-within-a-c-program"></a>Diepte teller in een C# programma gebruiken

Ga als volgt te werk om te controleren of `CCNOT` `T` diepte 5 heeft en `CCNOTDriver` `T` diepte 6 C# hebben, dan kunnen we de volgende code gebruiken:

```csharp 
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.useDepthCounter = true;
var sim = new QCTraceSimulator(config);
var res = CCNOTDriver.Run(sim).Result;

double tDepth = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<CCNOTDriver>(DepthCounter.Metrics.Depth);
```

Het eerste deel van het programma voert `CCNOTDriver`uit. In het tweede deel gebruiken we de methode `QCTraceSimulator.GetMetric` om de `T` diepte van `CCNOT` en `CCNOTDriver`te verkrijgen: 

```csharp
double tDepth = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<CCNOTDriver>(DepthCounter.Metrics.Depth);
```

Ten slotte kunnen we het volgende gebruiken voor het uitvoeren van alle statistieken die worden verzameld door `Depth Counter` in CSV-indeling:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a>Zie ook ##

- Het quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) -overzicht.
