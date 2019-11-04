---
title: Teller voor breedte | Quantum computer Trace Simulator | Microsoft Docs
description: Overzicht van kwantumcomputer-traceersimulator
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: ae0c0ec2e677be03dc8dc1497dc62ad9034295a4
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442414"
---
# <a name="width-counter"></a>Teller voor breedte

Het `Width Counter` telt het aantal qubits dat door elke bewerking wordt toegewezen en uitgeleend.
Alle bewerkingen van de naam ruimte `Microsoft.Quantum.Primitive` worden uitgedrukt in termen van één Qubit draaiing, T-Gates, single Qubit Clifford-poorten, CNOT-poorten en metingen van multi-Qubit Pauli observables. Sommige primitieve bewerkingen kunnen extra qubits toewijzen. U kunt bijvoorbeeld gestuurde `X` Gates of beheerde `T` poorten vermenigvuldigen. Laat ons het aantal extra qubits berekenen dat wordt toegewezen door de implementatie van een door vermenigvuldiging beheerde `X` Gate:

```qsharp
open Microsoft.Quantum.Primitive;
open Microsoft.Quantum.Arrays;
operation MultiControlledXDriver( numberOfQubits : Int ) : Unit {

    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a>Het gebruik van een breedte C# teller binnen een programma

Met vermenigvuldiging `X` die op een totaal van 5 qubits handelen, wordt 2 bijkomende qubits toegewezen en is de invoer breedte 5. Om te controleren of dit het geval is, kunnen we het volgende C# programma gebruiken:

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.useWidthCounter = true;
var sim = new QCTraceSimulator(config);
int totalNumberOfQubits = 5;
var res = MultiControlledXDriver.Run(sim, totalNumberOfQubits).Result;

double allocatedQubits = 
    sim.GetMetric<Primitive.X, MultiControlledXDriver>(
        WidthCounter.Metrics.ExtraWidth,
        functor: OperationFunctor.Controlled); 

double inputWidth =
    sim.GetMetric<Primitive.X, MultiControlledXDriver>(
        WidthCounter.Metrics.InputWidth,
        functor: OperationFunctor.Controlled);
```

Het eerste deel van het programma voert `MultiControlledXDriver`uit. In het tweede deel gebruiken we de methode `QCTraceSimulator.GetMetric` om het aantal toegewezen qubits te verkrijgen, evenals het aantal qubits dat wordt gecontroleerd `X` ontvangen als invoer. 

Ten slotte kunnen we het volgende gebruiken om alle statistieken die worden verzameld door de breedte teller in CSV-indeling uit te voeren:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a>Zie ook ##

- Het quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) -overzicht.
