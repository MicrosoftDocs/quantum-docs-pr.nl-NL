---
title: Ongeldig qubits use Checker-Quantum Development Kit
description: 'Meer informatie over de micro soft QDK ongeldig qubits use Checker, die gebruikmaakt van de Quantum Trace Simulator om uw Q #-code te controleren op mogelijk ongeldige qubits.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: fccf6d5784b587f4ad9b659e23027619acd06ffa
ms.sourcegitcommit: cdf67362d7b157254e6fe5c63a1c5551183fc589
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/21/2020
ms.locfileid: "86871090"
---
# <a name="quantum-trace-simulator-invalidated-qubits-use-checker"></a>Quantum Trace Simulator: ongeldig qubits use Checker

De ongeldig qubits use-controle is een onderdeel van de Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro). U kunt dit gebruiken om mogelijke fouten te detecteren in de code die is veroorzaakt door ongeldige qubits. 

## <a name="invalid-qubits"></a>Ongeldige qubits

Houd rekening met het volgende deel van Q # code voor het illustreren van de problemen die worden gedetecteerd door de ongeldig qubits-controle functie:

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

Wanneer u de `H` bewerking toepast op `q[0]` , wijst deze naar een reeds vrijgegeven Qubit. Dit kan leiden tot ongedefinieerd gedrag. Wanneer de ongeldig qubits-controle functie is ingeschakeld, wordt de uitzonde ring gegenereerd `InvalidatedQubitsUseCheckerException` als een bewerking wordt toegepast op een reeds vrijgegeven Qubit. Voor meer informatie raadpleegt u <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException>.

## <a name="invoking-the-invalidated-qubits-use-checker"></a>Het aanroepen van de ongeldig te controleren qubits use Checker

Als u de Quantum Trace Simulator wilt uitvoeren met de ongeldig qubits use-controle, moet u een <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instantie maken, de `UseInvalidatedQubitsUseChecker` eigenschap instellen op **True**en vervolgens een nieuw <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> exemplaar maken met `QCTraceSimulatorConfiguration` als de para meter. 

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
- De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException> API-verwijzing.