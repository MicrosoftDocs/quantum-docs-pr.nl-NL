---
title: Afzonderlijke invoer controle | Quantum computer Trace Simulator | Microsoft Docs
description: Overzicht van kwantumcomputer-traceersimulator
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
ms.openlocfilehash: 3c21a54f5da83bf1ea0792e79cc773be5fba71e8
ms.sourcegitcommit: f8d6d32d16c3e758046337fb4b16a8c42fb04c39
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2020
ms.locfileid: "76820960"
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

Wanneer de gebruiker dit programma bekijkt, wordt ervan uitgegaan dat de volg orde waarin `op1` en `op2` worden genoemd, niet van belang is omdat `q1` en `q2` verschillende qubits en bewerkingen op verschillende qubits werken. We gaan nu een voor beeld bekijken waarin deze bewerking wordt gebruikt:

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

Nu `op1` en `op2` beide zijn verkregen met behulp van gedeeltelijke toepassing en een Qubit delen. Wanneer de gebruiker `ApplyBoth` in het bovenstaande voor beeld aanroept, is de volg orde van `op1` en `op2` binnen `ApplyBoth`afhankelijk van het resultaat van de bewerking. Dit is zeker niet wat de gebruiker zou verwachten te doen. De `Distinct Inputs Checker` detecteert dergelijke situaties wanneer deze zijn ingeschakeld en genereren `DistinctInputsCheckerException`. Zie de API-documentatie op [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) voor meer informatie.

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a>De afzonderlijke invoer controle gebruiken in uw C# programma

Hier volgt een voor beeld van C# een stuur programma code voor het gebruik van de quantum computer Trace Simulator met de `Distinct Inputs Checker` ingeschakeld:

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

De klasse `QCTraceSimulatorConfiguration` slaat de configuratie van de quantum computer Trace Simulator op en kan worden ingesteld als een argument voor de `QCTraceSimulator`-constructor. Als `useDistinctInputsChecker` is ingesteld op True, wordt de `Distinct Inputs Checker` ingeschakeld. Zie de API-documentatie op [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) en [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) voor meer informatie.

## <a name="see-also"></a>Zie ook

- Het quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) -overzicht.
