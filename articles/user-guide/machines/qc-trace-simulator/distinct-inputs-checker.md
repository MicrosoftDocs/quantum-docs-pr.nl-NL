---
title: Afzonderlijke invoer controle-Quantum Development Kit
description: 'Meer informatie over de micro soft QDK DISTINCT inputs-controle, die gebruikmaakt van de Quantum Trace Simulator om uw Q #-code te controleren op mogelijke conflicten met gedeelde qubits.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
ms.openlocfilehash: 49a1ccc5f37acfeaa1ee08bd974be45a40a76f93
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871141"
---
# <a name="quantum-trace-simulator-distinct-inputs-checker"></a>Quantum Trace Simulator: DISTINCT-invoer controleprogramma

De DISTINCT-invoer controle maakt deel uit van de Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro). U kunt deze gebruiken voor het detecteren van mogelijke fouten in de code die wordt veroorzaakt door conflicten met gedeelde qubits. 

## <a name="conflicts-with-shared-qubits"></a>Conflicten met gedeelde qubits

Houd rekening met het volgende stukje Q #-code om de problemen te illustreren die worden gedetecteerd door de afzonderlijke invoer controle:

```qsharp
operation ApplyBoth(
    q1 : Qubit,
    q2 : Qubit,
    op1 : (Qubit => Unit),
    op2 : (Qubit => Unit))
: Unit {
    op1(q1);
    op2(q2);
}
```

Wanneer u dit programma bekijkt, kunt u ervan uitgaan dat de volg orde waarin deze aanroept `op1` en `op2` niet van belang is, omdat `q1` en `q2` andere qubits en bewerkingen op verschillende qubits werken. 

Bekijk nu het volgende voor beeld:

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

Houd er rekening mee dat `op1` `op2` beide zijn verkregen met behulp van gedeeltelijke toepassing en een Qubit delen. Wanneer u `ApplyBoth` dit voor beeld aanroept, is het resultaat van de bewerking afhankelijk van de volg orde van `op1` en `op2` binnen `ApplyBoth` -niet wat u verwacht te doen. Wanneer u de afzonderlijke invoer controle inschakelt, worden dergelijke situaties gedetecteerd en wordt er een gegenereerd `DistinctInputsCheckerException` . Zie <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> de Q # API-bibliotheek voor meer informatie.

## <a name="invoking-the-distinct-inputs-checker"></a>De afzonderlijke invoer controle aanroepen

Als u de Quantum Trace Simulator wilt uitvoeren met de afzonderlijke invoer controle, moet u een <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instantie maken, de `UseDistinctInputsChecker` eigenschap instellen op **True**en vervolgens een nieuw <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> exemplaar maken met `QCTraceSimulatorConfiguration` als de para meter. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDistinctInputsChecker = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-distinct-inputs-checker-in-a-c-host-program"></a>De DISTINCT-invoer controle gebruiken in een C#-hostprogramma

Hier volgt een voor beeld van een C#-hostprogramma dat gebruikmaakt van de Quantum Trace Simulator, waarbij de afzonderlijke invoer controle is ingeschakeld:

```csharp
using Microsoft.Quantum.Simulation.Core;
using Microsoft.Quantum.Simulation.Simulators;
using Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators;

namespace Quantum.MyProgram
{
    class Driver
    {
        static void Main(string[] args)
        {
            var traceSimCfg = new QCTraceSimulatorConfiguration();
            traceSimCfg.UseDistinctInputsChecker = true; //enables distinct inputs checker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

## <a name="see-also"></a>Zie ook

- Het Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Overview (Engelstalig).
- De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-verwijzing.
- De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-verwijzing.
- De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> API-verwijzing.
