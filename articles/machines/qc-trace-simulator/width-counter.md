---
title: Teller voor breedte | Quantum computer Trace Simulator | Microsoft Docs
description: Overzicht van kwantumcomputer-traceersimulator
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: 9c3601e74eec17bd6b463e90f8f3085c959d6f95
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820365"
---
# <a name="width-counter"></a>Teller voor breedte

Het `Width Counter` telt het aantal qubits dat door elke bewerking wordt toegewezen en uitgeleend.
Alle bewerkingen van de naam ruimte `Microsoft.Quantum.Intrinsic` worden uitgedrukt in termen van één Qubit draaiing, T-Gates, single Qubit Clifford-poorten, CNOT-poorten en metingen van multi-Qubit Pauli observables. Sommige primitieve bewerkingen kunnen extra qubits toewijzen. U kunt bijvoorbeeld gestuurde `X` Gates of beheerde `T` poorten vermenigvuldigen. Laat ons het aantal extra qubits berekenen dat wordt toegewezen door de implementatie van een door vermenigvuldiging beheerde `X` Gate:

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
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

Het eerste deel van het programma voert `ApplyMultiControlledX`uit. In het tweede deel gebruiken we de methode `QCTraceSimulator.GetMetric` om het aantal toegewezen qubits te verkrijgen, evenals het aantal qubits dat wordt gecontroleerd `X` ontvangen als invoer. 

Ten slotte kunnen we het volgende gebruiken om alle statistieken die worden verzameld door de breedte teller in CSV-indeling uit te voeren:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a>Zie ook ##

- Het quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) -overzicht.
