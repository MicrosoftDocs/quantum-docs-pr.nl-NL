---
title: Controle op het gebruik van ongeldige qubits
description: 'Meer informatie over de QDK qubits use Checker van micro soft, waarmee uw Q #-code wordt gecontroleerd op mogelijk ongeldige qubits.'
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits
ms.openlocfilehash: e2bbb12448e27f28db030a0084302fb24f46f26b
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274902"
---
# <a name="invalidated-qubits-use-checker"></a><span data-ttu-id="9152c-103">Qubits use-controle is ongeldig</span><span class="sxs-lookup"><span data-stu-id="9152c-103">Invalidated Qubits Use Checker</span></span>

<span data-ttu-id="9152c-104">Het `Invalidated Qubits Use Checker` maakt deel uit van de quantum computer [TraceSimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) die is ontworpen voor het detecteren van mogelijke fouten in de code.</span><span class="sxs-lookup"><span data-stu-id="9152c-104">The `Invalidated Qubits Use Checker` is a part of the quantum computer [TraceSimulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) designed for detecting potential bugs in the code.</span></span> <span data-ttu-id="9152c-105">Houd rekening met het volgende stukje Q #-code om de problemen te illustreren die worden gedetecteerd door de `Invalidated Qubits Use Checker` .</span><span class="sxs-lookup"><span data-stu-id="9152c-105">Consider the following piece of Q# code to illustrate the issues detected by the `Invalidated Qubits Use Checker`.</span></span>

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

<span data-ttu-id="9152c-106">Wanneer `H` wordt toegepast op `q[0]` het item, verwijst naar een al vrijgegeven Qubit.</span><span class="sxs-lookup"><span data-stu-id="9152c-106">When `H` is applied to `q[0]` it points to an already released qubit.</span></span> <span data-ttu-id="9152c-107">Dit kan ongedefinieerd gedrag veroorzaken.</span><span class="sxs-lookup"><span data-stu-id="9152c-107">This can cause undefined behavior.</span></span> <span data-ttu-id="9152c-108">Als de `Invalidated Qubits Use Checker` is ingeschakeld, wordt de uitzonde ring `InvalidatedQubitsUseCheckerException` gegenereerd als een bewerking wordt toegepast op een reeds vrijgegeven Qubit.</span><span class="sxs-lookup"><span data-stu-id="9152c-108">When the `Invalidated Qubits Use Checker` is enabled, the exception `InvalidatedQubitsUseCheckerException` will be thrown if an operation is applied to an already released qubit.</span></span> <span data-ttu-id="9152c-109">Zie de API-documentatie op [InvalidatedQubitsUseCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="9152c-109">See the API documentation on [InvalidatedQubitsUseCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException) for more details.</span></span>

## <a name="using-the-invalidated-qubits-use-checker-in-your-c-program"></a><span data-ttu-id="9152c-110">De ongeldig qubits use-controle gebruiken in uw C#-programma</span><span class="sxs-lookup"><span data-stu-id="9152c-110">Using the Invalidated Qubits Use Checker in your C# Program</span></span>

<span data-ttu-id="9152c-111">Hier volgt een voor beeld van een code van een C#-stuur programma voor het gebruik van de quantum computer `Trace
Simulator` met de `Invalidated Qubits Use Checker` ingeschakelde:</span><span class="sxs-lookup"><span data-stu-id="9152c-111">The following is an example of C# driver code for using the quantum computer `Trace
Simulator` with the `Invalidated Qubits Use Checker` enabled:</span></span> 

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

<span data-ttu-id="9152c-112">De klasse `QCTraceSimulatorConfiguration` slaat de configuratie van de quantum computer Trace Simulator op en kan worden ingesteld als een argument voor de `QCTraceSimulator` constructor.</span><span class="sxs-lookup"><span data-stu-id="9152c-112">The class `QCTraceSimulatorConfiguration` stores the configuration of the quantum computer trace simulator and can be provided as an argument for the `QCTraceSimulator` constructor.</span></span> <span data-ttu-id="9152c-113">Wanneer `useInvalidatedQubitsUseChecker` is ingesteld op True, `Invalidated Qubits Use Checker` wordt de is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="9152c-113">When `useInvalidatedQubitsUseChecker` is set to true the `Invalidated Qubits Use Checker` is enabled.</span></span> <span data-ttu-id="9152c-114">Zie de API-documentatie op [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) en [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="9152c-114">See the API documentation on [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) and [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) for more details.</span></span>

## <a name="see-also"></a><span data-ttu-id="9152c-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9152c-115">See also</span></span> ##

- <span data-ttu-id="9152c-116">Het quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) -overzicht.</span><span class="sxs-lookup"><span data-stu-id="9152c-116">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>