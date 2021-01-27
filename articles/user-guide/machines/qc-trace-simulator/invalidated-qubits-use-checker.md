---
title: Ongeldig qubits use Checker-Quantum Development Kit
description: Meer informatie over de micro soft QDK qubits use Checker, die gebruikmaakt van de Quantum Trace Simulator om uw code te controleren op Q# potentieel ongeldige qubits.
author: vadym-kl
ms.author: vadym
ms.date: 06/25/2020
ms.topic: conceptual
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
no-loc:
- Q#
- $$v
ms.openlocfilehash: 9014097ace7c9f19d93a92372da40f71fa7f87ee
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858610"
---
# <a name="quantum-trace-simulator-invalidated-qubits-use-checker"></a>Quantum Trace Simulator: ongeldig qubits use Checker

De ongeldig qubits use-controle is een onderdeel van de Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro). U kunt dit gebruiken om mogelijke fouten te detecteren in de code die is veroorzaakt door ongeldige qubits. 

## <a name="invalid-qubits"></a>Ongeldige qubits

Houd rekening met het volgende Q# code fragment voor een illustratie van de problemen die worden gedetecteerd door de ongeldig qubits use Checker:

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

Wanneer u de `H` bewerking toepast op `q[0]` , wijst deze naar een reeds vrijgegeven Qubit. Dit kan leiden tot ongedefinieerd gedrag. Wanneer de ongeldig qubits-controle functie is ingeschakeld, wordt de uitzonde ring gegenereerd `InvalidatedQubitsUseCheckerException` als een bewerking wordt toegepast op een reeds vrijgegeven Qubit. Voor meer informatie raadpleegt u <xref:Microsoft.Quantum.Simulation.QCTraceSimulatorRuntime.InvalidatedQubitsUseCheckerException>.

## <a name="invoking-the-invalidated-qubits-use-checker"></a>Het aanroepen van de ongeldig te controleren qubits use Checker

Als u de Quantum Trace Simulator wilt uitvoeren met de ongeldig qubits use-controle, moet u een <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instantie maken, de `UseInvalidatedQubitsUseChecker` eigenschap instellen op **True** en vervolgens een nieuw <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> exemplaar maken met `QCTraceSimulatorConfiguration` als de para meter. 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseInvalidatedQubitsUseChecker = true;
var sim = new QCTraceSimulator(config);
```


## <a name="using-the-invalidated-qubits-use-checker-in-a-c-host-program"></a>De ongeldig qubits use Checker gebruiken in een C#-hostprogramma

Hier volgt een voor beeld van C#-hostgroepen die gebruikmaken van de Quantum Trace Simulator waarbij de ongeldig qubits use-controle is ingeschakeld: 

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
            traceSimCfg.UseInvalidatedQubitsUseChecker = true; // enables UseInvalidatedQubitsUseChecker
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
- De <xref:Microsoft.Quantum.Simulation.QCTraceSimulatorRuntime.InvalidatedQubitsUseCheckerException> API-verwijzing.
