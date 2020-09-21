---
title: Teller voor primitieve bewerkingen-Quantum Development Kit
description: Meer informatie over het micro soft QDK primitieve bewerkings item, dat gebruikmaakt van de Quantum Trace Simulator om primitieve processen bij te houden die worden gebruikt door bewerkingen in een Q# programma.
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.primitive-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: 8ee9ce25e680112e2f3c68d82ae9267c1b0fb355
ms.sourcegitcommit: 9b0d1ffc8752334bd6145457a826505cc31fa27a
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/21/2020
ms.locfileid: "90835975"
---
# <a name="quantum-trace-simulator-primitive-operations-counter"></a>Quantum Trace Simulator: primitieve bewerkingen teller

Het teller primitieve bewerking maakt deel uit van de Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro). Hiermee wordt het aantal primitieve processen geteld dat wordt gebruikt door elke bewerking die wordt aangeroepen in een Quantum programma. 

Alle <xref:microsoft.quantum.intrinsic> bewerkingen worden uitgedrukt in termen van Qubit draaiingen, T-bewerkingen, single-Qubit Clifford-bewerkingen, CNOT bewerkingen en metingen van multi-Qubit Pauli observables. Met het teller primitieve bewerkingen worden statistieken geaggregeerd en verzameld over alle randen van de [aanroep grafiek](https://en.wikipedia.org/wiki/Call_graph)van de bewerking.

## <a name="invoking-the-primitive-operation-counter"></a>Het item primitieve bewerking aanroepen

Als u de Quantum Trace Simulator wilt uitvoeren met het teller primitieve bewerking, moet u een <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> exemplaar maken, de `UsePrimitiveOperationsCounter` eigenschap instellen op **waar**en vervolgens een nieuw <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> exemplaar maken met de `QCTraceSimulatorConfiguration` as-para meter.

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-primitive-operation-counter-in-a-c-host-program"></a>Het teller primitieve bewerking in een C#-hostprogramma gebruiken

Het C#-voor beeld dat volgt in deze sectie telt het aantal <xref:microsoft.quantum.intrinsic.t> bewerkingen dat nodig is voor het implementeren van de <xref:microsoft.quantum.intrinsic.ccnot> bewerking, op basis van de volgende Q# voorbeeld code:

```qsharp
open Microsoft.Quantum.Intrinsic;
operation ApplySampleWithCCNOT() : Unit {

    using (qubits = Qubit[3]) {
        CCNOT(qubits[0], qubits[1], qubits[2]);
        T(qubits[0]);
    }
}
```

`CCNOT` `T` `ApplySampleWithCCNOT` `T` Gebruik de volgende C#-code om te controleren dat zeven bewerkingen vereist en acht bewerkingen uitvoert:

```csharp 
// using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;
// using System.Diagnostics;
var config = new QCTraceSimulatorConfiguration();
config.UsePrimitiveOperationsCounter = true;
var sim = new QCTraceSimulator(config);
var res = ApplySampleWithCCNOT.Run(sim).Result;

double tCountAll = sim.GetMetric<ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
double tCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.T);
```

Het eerste deel van het programma wordt uitgevoerd `ApplySampleWithCCNOT` . In het tweede deel wordt gebruikgemaakt [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) van de methode voor het ophalen van het aantal bewerkingen dat wordt `T` uitgevoerd door `ApplySampleWithCCNOT` : 

Wanneer u `GetMetric` met twee type parameters aanroept, wordt de waarde van de metriek geretourneerd die is gekoppeld aan een bepaalde rand van de oproep grafiek. In het voor gaande voor beeld roept het programma de `Primitive.CCNOT` bewerking binnen `ApplySampleWithCCNOT` en daarom bevat de oproep grafiek de rand `<Primitive.CCNOT, ApplySampleWithCCNOT>` . 

`CNOT`Voeg de volgende regel toe om het aantal gebruikte bewerkingen op te halen:
```csharp
double cxCount = sim.GetMetric<Primitive.CCNOT, ApplySampleWithCCNOT>(PrimitiveOperationsGroupsNames.CX);
```

Ten slotte kunt u alle statistieken die door het item primitieve bewerkingen zijn verzameld, in CSV-indeling uitvoeren met het volgende:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.primitiveOperationsCounter];
```

## <a name="see-also"></a>Zie tevens

- Het Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Overview (Engelstalig).
- De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-verwijzing.
- De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-verwijzing.
- De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.PrimitiveOperationsGroupsNames> API-verwijzing.