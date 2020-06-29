---
title: Diepte teller
description: Meer informatie over het micro soft QDK depth Counter, waarmee u het aantal niveaus van elke bewerking die wordt aangeroepen in een Quantum programma, kunt verzamelen.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.depth-counter
ms.openlocfilehash: 0029a00e6a3563dc542daeda2afa7cabf42441fb
ms.sourcegitcommit: af10179284967bd7a72a52ae7e1c4da65c7d128d
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/26/2020
ms.locfileid: "85415256"
---
# <a name="depth-counter"></a>Diepte teller

De `Depth Counter` maakt deel uit van de quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).
Het wordt gebruikt voor het verzamelen van aantallen die de laagste grens van elke bewerking vertegenwoordigen die in een Quantum programma wordt aangeroepen. Alle bewerkingen van <xref:microsoft.quantum.intrinsic> worden uitgedrukt in termen van enkelvoudige Qubit rotaties, T-poorten, enkelvoudige Qubit Clifford-poorten, CNOT poorten en metingen van multi-Qubit Pauli observables. Gebruikers kunnen de diepte instellen voor elk van de primitieve bewerkingen via het `gateTimes` veld van <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> .

Standaard hebben alle bewerkingen diepte 0, met uitzonde ring van de T-poort, die diepte 1 heeft. Dit betekent dat standaard alleen de w-diepte van bewerkingen wordt berekend (vaak gewenst). Verzamelde statistieken worden geaggregeerd over alle randen van de operations call-grafiek. 

Laat ons nu de <xref:microsoft.quantum.intrinsic.t> diepte van de <xref:microsoft.quantum.intrinsic.ccnot> bewerking berekenen. We zullen de volgende Q #-voorbeeld code gebruiken:

```qsharp
open Microsoft.Quantum.Intrinsic;

operation ApplySampleWithCCNOT() : Unit {
    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

## <a name="using-depth-counter-within-a-c-program"></a>Diepte teller gebruiken binnen een C#-programma

Als u wilt controleren of `CCNOT` `T` de diepte 5 en `ApplySampleWithCCNOT` diepte 6 zijn, kunt u `T` de volgende C#-code gebruiken:

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

Het eerste deel van het programma wordt uitgevoerd `ApplySampleWithCCNOT` . In het tweede deel gebruiken we de methode `QCTraceSimulator.GetMetric` voor het verkrijgen `T` van de diepte van `CCNOT` en `ApplySampleWithCCNOT` : 

```csharp
double tDepth = sim.GetMetric<Intrinsic.CCNOT, ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
double tDepthAll = sim.GetMetric<ApplySampleWithCCNOT>(DepthCounter.Metrics.Depth);
```

Ten slotte kunnen we het volgende gebruiken voor het uitvoeren van alle statistieken die worden verzameld met `Depth Counter` in CSV-indeling:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.depthCounter];
```

## <a name="see-also"></a>Zie ook ##

- Het quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) -overzicht.
