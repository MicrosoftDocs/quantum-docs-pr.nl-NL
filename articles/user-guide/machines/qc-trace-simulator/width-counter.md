---
title: Counter-Quantum Development Kit
description: Meer informatie over de micro soft QDK width Counter, die gebruikmaakt van de Quantum Trace Simulator voor het tellen van het aantal qubits dat is toegewezen en uitgeleend door bewerkingen in een Q# programma.
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: e9a526ee1440544aace922bd83c6ea39cb83c1ae
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858583"
---
# <a name="quantum-trace-simulator-width-counter"></a>Quantum Trace Simulator: breedte teller

De teller voor de breedte is een onderdeel van de Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro). U kunt deze gebruiken om het aantal toegewezen qubits te tellen dat door elke bewerking in een programma wordt verdeeld en uitgeleend Q# . Met sommige primitieve bewerkingen kunt u extra qubits toewijzen, bijvoorbeeld gecontroleerde `X` bewerkingen of beheerde `T` bewerkingen.

## <a name="invoking-the-width-counter"></a>Aanroepen van de teller voor breedte

Als u de Quantum Trace Simulator met de breedte teller wilt uitvoeren, moet u een <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> exemplaar maken, de `UseWidthCounter` eigenschap instellen op **True** en vervolgens een nieuw <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> exemplaar maken met de `QCTraceSimulatorConfiguration` as-para meter. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-width-counter-in-a-c-host-program"></a>De teller width gebruiken in een C#-hostprogramma

In het C#-voor beeld dat volgt in deze sectie wordt het aantal extra qubits berekend dat wordt toegewezen door de implementatie van een door vermenigvuldiging beheerde <xref:Microsoft.Quantum.Intrinsic.X> bewerking, op basis van de volgende Q# voorbeeld code:

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

Met de bewerking vermenigvuldigen <xref:Microsoft.Quantum.Intrinsic.X> wordt een totaal van vijf qubits toegepast, worden er twee [bijkomende qubits](xref:microsoft.quantum.glossary#ancilla)toegewezen, en heeft dit een invoer breedte van **5**. Gebruik het volgende C#-programma om de aantallen te controleren:

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
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

Het eerste deel van het programma voert de `ApplyMultiControlledX` bewerking uit. In het tweede deel wordt de [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) methode gebruikt om het aantal toegewezen qubits op te halen, evenals het aantal qubits dat de `Controlled X` bewerking heeft ontvangen als invoer. 

Ten slotte kunt u alle statistieken die worden verzameld door de teller breedte in CSV-indeling uitvoeren met het volgende:
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a>Zie ook

- Het Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Overview (Engelstalig).
- De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-verwijzing.
- De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-verwijzing.
- De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.WidthCounter> API-verwijzing.
