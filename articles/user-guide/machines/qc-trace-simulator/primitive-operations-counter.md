---
title: Teller voor primitieve bewerkingen
description: Meer informatie over het item micro soft QDK primitieve bewerking, waarmee het aantal primitieve uitvoeringen wordt bijgehouden dat door bewerkingen in een Quantum programma wordt gebruikt.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
ms.openlocfilehash: 8bdb0aed370e72b58b23025f1685ad7ce1a77a43
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274892"
---
# <a name="primitive-operations-counter"></a>Teller voor primitieve bewerkingen  

De `Primitive Operations Counter` maakt deel uit van de quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro). Het telt het aantal primitieve uitvoeringen dat wordt gebruikt door elke bewerking die wordt aangeroepen in een Quantum programma. Alle bewerkingen van `Microsoft.Quantum.Intrinsic` worden uitgedrukt in termen van enkelvoudige Qubit rotaties, T-poorten, enkelvoudige Qubit Clifford-poorten, CNOT poorten en metingen van multi-Qubit Pauli observables. Verzamelde statistieken worden geaggregeerd over de randen van de operations call-grafiek. We tellen nu het aantal `T` poorten dat nodig is voor het implementeren van de `CCNOT` bewerking. 

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    } 
}
```

## <a name="using-the-primitive-operations-counter-within-a-c-program"></a>Het item primitieve bewerkingen in een C#-programma gebruiken

Om te controleren of `CCNOT` er zeven `T` Gates vereist zijn en dat `ApplySampleWithCCNOT` `T` er 8 Gates worden uitgevoerd, kunnen we de volgende C#-code gebruiken:

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.usePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

Het eerste deel van het programma wordt uitgevoerd `ApplySampleWithCCNOT` . In het tweede deel wordt de methode gebruikt `QCTraceSimulator.GetMetric` om het aantal T-poorten te verkrijgen dat wordt uitgevoerd door `ApplySampleWithCCNOT` : 

```csharp
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

Wanneer `GetMetric` wordt aangeroepen met twee type parameters, wordt de waarde van de metriek geretourneerd die is gekoppeld aan een bepaalde rand van de oproep grafiek. In de voor beeld-bewerking wordt de rand van de `Primitive.CCNOT` `ApplySampleWithCCNOT` aanroep grafiek genoemd `<Primitive.CCNOT, ApplySampleWithCCNOT>` . 

Om het aantal `CNOT` gebruikte poorten te verkrijgen, kunnen we de volgende regel toevoegen:
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

Ten slotte kunnen we het volgende gebruiken voor het uitvoeren van alle statistieken die worden verzameld door de poort teller in CSV-indeling:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a>Zie ook ##

- Het quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) -overzicht.
