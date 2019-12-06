---
title: Ongeldig qubits-gebruikcontrole programma | Quantum computer Trace Simulator | Microsoft Docs
description: Overzicht van kwantumcomputer-traceersimulator
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: 283cc7d7d88f731f40fa396c38ae5ea8dd90537f
ms.sourcegitcommit: 27c9bf1aae923527aa5adeaee073cb27d35c0ca1
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2019
ms.locfileid: "74863177"
---
# <a name="invalidated-qubits-use-checker"></a>Qubits use-controle is ongeldig

De `Invalidated Qubits Use Checker` maakt deel uit van de quantum computer [TraceSimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) die is ontworpen voor het detecteren van mogelijke fouten in de code. Houd rekening met het volgende gedeelte van Q #-code om de problemen te illustreren die worden gedetecteerd door de `Invalidated Qubits Use Checker`.

```qsharp
operation UseReleasedQubit () : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

Als `H` wordt toegepast op `q[0]`, wijst het naar een al vrijgegeven Qubit. Dit kan ongedefinieerd gedrag veroorzaken. Wanneer de `Invalidated Qubits Use Checker` is ingeschakeld, wordt de uitzonde ring `InvalidatedQubitsUseCheckerException` gegenereerd als er een bewerking wordt toegepast op een reeds vrijgegeven Qubit. Zie de API-documentatie op [InvalidatedQubitsUseCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) voor meer informatie.

## <a name="using-the-invalidated-qubits-use-checker-in-your-c-program"></a>De ongeldig qubits use checker in uw C# programma gebruiken

Hier volgt een voor beeld van C# een stuur programma code voor het gebruik van de quantum computer `Trace
Simulator` met de `Invalidated Qubits Use Checker` ingeschakeld: 

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
            traceSimCfg.useInvalidatedQubitsUseChecker = true; // enables useInvalidatedQubitsUseChecker
            QCTraceSimulator sim = new QCTraceSimulator(traceSimCfg);
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

De klasse `QCTraceSimulatorConfiguration` slaat de configuratie van de quantum computer Trace Simulator op en kan worden ingesteld als een argument voor de `QCTraceSimulator`-constructor. Als `useInvalidatedQubitsUseChecker` is ingesteld op True, wordt de `Invalidated Qubits Use Checker` ingeschakeld. Zie de API-documentatie op [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) en [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) voor meer informatie.

## <a name="see-also"></a>Zie ook ##

- Het quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) -overzicht.
