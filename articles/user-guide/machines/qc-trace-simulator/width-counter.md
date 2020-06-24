---
title: Teller voor breedte
description: Meer informatie over de micro soft QDK width Counter, waarmee het aantal qubits wordt geteld dat is toegewezen aan en uitgeleend door elke bewerking in een Quantum programma.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
ms.openlocfilehash: a76292222950310acc90dded02980e4a5b792e76
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274895"
---
# <a name="width-counter"></a>Teller voor breedte

Het `Width Counter` telt het aantal qubits dat wordt toegewezen en uitgeleend door elke bewerking.
Alle bewerkingen van de `Microsoft.Quantum.Intrinsic` naam ruimte worden uitgedrukt in termen van één Qubit draaiing, T-Gates, single Qubit Clifford-poorten, CNOT-poorten en metingen van multi-Qubit Pauli observables. Sommige primitieve bewerkingen kunnen extra qubits toewijzen. Bijvoorbeeld gestuurde `X` Gates of gestuurde poorten vermenigvuldigen `T` . Laat ons het aantal extra qubits berekenen dat is toegewezen door de implementatie van een door een beheerste poort van vermenigvuldiging `X` :

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

## <a name="using-width-counter-within-a-c-program"></a>De teller width gebruiken binnen een C#-programma

Met vermenigvuldiging `X` met een totaal van 5 qubits wordt 2 bijkomende qubits toegewezen en is de invoer breedte 5. Om te controleren of dit het geval is, kunnen we het volgende C#-programma gebruiken:

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

Het eerste deel van het programma wordt uitgevoerd `ApplyMultiControlledX` . In het tweede deel gebruiken we de methode `QCTraceSimulator.GetMetric` om het aantal toegewezen qubits te verkrijgen, evenals het aantal qubits dat is gecontroleerd `X` als invoer. 

Ten slotte kunnen we het volgende gebruiken om alle statistieken die worden verzameld door de breedte teller in CSV-indeling uit te voeren:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a>Zie ook ##

- Het quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) -overzicht.
