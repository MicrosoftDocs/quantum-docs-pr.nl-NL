---
title: Primitieve bewerkingen teller | Quantum computer Trace Simulator | Microsoft Docs
description: Overzicht van quantum computer Trace Simulator
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
ms.openlocfilehash: b7ec8b0d7a713051e36cb778c087050f0257710f
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184879"
---
# <a name="primitive-operations-counter"></a>Teller voor primitieve bewerkingen  

De `Primitive Operations Counter` maakt deel uit van de quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro). Het telt het aantal primitieve uitvoeringen dat wordt gebruikt door elke bewerking die wordt aangeroepen in een Quantum programma. Alle bewerkingen van `Microsoft.Quantum.Primitive` worden uitgedrukt in termen van één Qubit rotatie, T-poorten, enkelvoudige Qubit Clifford-poorten, CNOT poorten en metingen van multi-Qubit Pauli observables. Verzamelde statistieken worden geaggregeerd over de randen van de operations call-grafiek. We tellen nu hoeveel `T` Gates nodig zijn voor het implementeren van de `CCNOT` bewerking. 

```qsharp
open Microsoft.Quantum.Primitive;
operation CCNOTDriver() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    } 
}
```

## <a name="using-the-primitive-operations-counter-within-a-c-program"></a>Het item primitieve bewerkingen in een C# programma gebruiken

Ga als volgt te werk om te controleren of `CCNOT` enige 7 `T` poorten vereist en dat `CCNOTDriver` acht `T` poorten worden C# uitgevoerd, kunnen we de volgende code gebruiken:

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.usePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = CCNOTDriver.Run(sim).Result;

double tCountAll = sim.GetMetric<CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
```

Het eerste deel van het programma voert `CCNOTDriver`uit. In het tweede deel gebruiken we de methode `QCTraceSimulator.GetMetric` om het aantal T-poorten te verkrijgen dat door `CCNOTDriver`wordt uitgevoerd: 

```csharp
double tCount = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
double tCountAll = sim.GetMetric<CCNOTDriver>(PrimitiveOperationsGroupsNames.T);
```

Als `GetMetric` wordt aangeroepen met twee type parameters, wordt de waarde van de metriek geretourneerd die is gekoppeld aan een bepaalde rand van de oproep grafiek. In de voorbeeld bewerking `Primitive.CCNOT` wordt aangeroepen in `CCNOTDriver`, waardoor de oproep grafiek de rand `<Primitive.CCNOT,CCNOTDriver>`bevat. 

Om het aantal `CNOT` gebruikte poorten te verkrijgen, kunnen we de volgende regel toevoegen:
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, CCNOTDriver>(PrimitiveOperationsGroupsNames.CX);
```

Ten slotte kunnen we het volgende gebruiken voor het uitvoeren van alle statistieken die worden verzameld door de poort teller in CSV-indeling:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a>Zie ook ##

- Het quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) -overzicht.
