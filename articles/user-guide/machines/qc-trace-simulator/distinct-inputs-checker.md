---
title: Afzonderlijke invoer controle
description: 'Meer informatie over de micro soft QDK DISTINCT inputs-controle, waarmee uw Q #-code wordt gecontroleerd op mogelijke conflicten met gedeelde qubits.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
ms.openlocfilehash: 11a0573242c8afb12f242aa3be5f9cff18290452
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274932"
---
# <a name="distinct-inputs-checker"></a>Afzonderlijke invoer controle

De `Distinct Inputs Checker` maakt deel uit van de quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro). Het is ontworpen voor het detecteren van mogelijke fouten in de code. Houd rekening met de volgende Q #-code om de problemen te illustreren die door dit pakket worden gedetecteerd:

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

Wanneer de gebruiker dit programma bekijkt, wordt ervan uitgegaan dat de volg orde waarin `op1` en `op2` worden aangeroepen, niet van belang is omdat `q1` en `q2` andere qubits en bewerkingen zijn die optreden op verschillende qubits. We gaan nu een voor beeld bekijken waarin deze bewerking wordt gebruikt:

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

Nu `op1` en `op2` zijn beide verkregen met behulp van gedeeltelijke toepassing en delen ze een Qubit. Wanneer de gebruiker `ApplyBoth` in het bovenstaande voor beeld belt, is het resultaat van de bewerking afhankelijk van de volg orde van `op1` en `op2` in `ApplyBoth` . Dit is zeker niet wat de gebruiker zou verwachten te doen. De `Distinct Inputs Checker` detecteert dergelijke situaties wanneer deze zijn ingeschakeld en worden gegenereerd `DistinctInputsCheckerException` . Zie de API-documentatie op [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) voor meer informatie.

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a>De DISTINCT-invoer controle gebruiken in uw C#-programma

Hier volgt een voor beeld van een C#-stuur programma voor het gebruik van de quantum computer Trace Simulator met de `Distinct Inputs Checker` ingeschakeld:

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
            traceSimCfg.useDistinctInputsChecker = true; //enables distinct inputs checker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

De klasse `QCTraceSimulatorConfiguration` slaat de configuratie van de quantum computer Trace Simulator op en kan worden ingesteld als een argument voor de `QCTraceSimulator` constructor. Wanneer `useDistinctInputsChecker` is ingesteld op True, `Distinct Inputs Checker` wordt de is ingeschakeld. Zie de API-documentatie op [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) en [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) voor meer informatie.

## <a name="see-also"></a>Zie ook

- Het quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) -overzicht.
