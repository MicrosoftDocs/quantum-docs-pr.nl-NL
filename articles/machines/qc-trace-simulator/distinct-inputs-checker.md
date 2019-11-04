---
title: Afzonderlijke invoer controle | Quantum computer Trace Simulator | Microsoft Docs
description: Overzicht van quantum computer Trace Simulator
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.distinct-inputs
ms.openlocfilehash: 0df28f6d74279db4678c3485a23a9341680eec52
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73184692"
---
# <a name="distinct-inputs-checker"></a><span data-ttu-id="81d83-103">Afzonderlijke invoer controle</span><span class="sxs-lookup"><span data-stu-id="81d83-103">Distinct Inputs Checker</span></span>

<span data-ttu-id="81d83-104">De `Distinct Inputs Checker` maakt deel uit van de quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span><span class="sxs-lookup"><span data-stu-id="81d83-104">The `Distinct Inputs Checker` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="81d83-105">Het is ontworpen voor het detecteren van mogelijke fouten in de code.</span><span class="sxs-lookup"><span data-stu-id="81d83-105">It is designed for detecting potential bugs in the code.</span></span> <span data-ttu-id="81d83-106">Houd rekening met de volgende Q #-code om de problemen te illustreren die door dit pakket worden gedetecteerd:</span><span class="sxs-lookup"><span data-stu-id="81d83-106">Consider the following piece of Q# code to illustrate the issues detected by this package:</span></span>

```qsharp
operation DoBoth(q1 : Qubit, q2 : Qubit, op1 : (Qubit => Unit), op2 : (Qubit => Unit)) : Unit {

    op1(q1);
    op2(q2);
}
```

<span data-ttu-id="81d83-107">Wanneer de gebruiker dit programma bekijkt, wordt ervan uitgegaan dat de volg orde waarin `op1` en `op2` worden genoemd, niet van belang is omdat `q1` en `q2` verschillende qubits en bewerkingen op verschillende qubits werken.</span><span class="sxs-lookup"><span data-stu-id="81d83-107">When the user looks at this program, they assume that the order in which `op1` and `op2` are called does not matter because `q1` and `q2` are different qubits and operations acting on different qubits commute.</span></span> <span data-ttu-id="81d83-108">We gaan nu een voor beeld bekijken waarin deze bewerking wordt gebruikt:</span><span class="sxs-lookup"><span data-stu-id="81d83-108">Let us now consider an example, where this operation is used:</span></span>

```qsharp
operation DisctinctQubitCaptured2Test () : Unit {

    using (q = Qubit[3]) {
        let op1 = CNOT(_, q[1]);
        let op2 = CNOT(q[1], _);
        DoBoth(q[0], q[2], op1, op2);
    }
}
```

<span data-ttu-id="81d83-109">Nu `op1` en `op2` beide zijn verkregen met behulp van gedeeltelijke toepassing en een Qubit delen.</span><span class="sxs-lookup"><span data-stu-id="81d83-109">Now `op1` and `op2` are both obtained using partial application and share a qubit.</span></span> <span data-ttu-id="81d83-110">Wanneer de gebruiker `DoBoth` in het bovenstaande voor beeld aanroept, is de volg orde van `op1` en `op2` binnen `DoBoth`afhankelijk van het resultaat van de bewerking.</span><span class="sxs-lookup"><span data-stu-id="81d83-110">When the user calls `DoBoth` in the example above the result of the operation will depend on the order of `op1` and `op2` inside `DoBoth`.</span></span> <span data-ttu-id="81d83-111">Dit is zeker niet wat de gebruiker zou verwachten te doen.</span><span class="sxs-lookup"><span data-stu-id="81d83-111">This is definitely not what the user would expect to happen.</span></span> <span data-ttu-id="81d83-112">De `Distinct Inputs Checker` detecteert dergelijke situaties wanneer deze zijn ingeschakeld en genereren `DistinctInputsCheckerException`.</span><span class="sxs-lookup"><span data-stu-id="81d83-112">The `Distinct Inputs Checker` will detect such situations when enabled and will throw `DistinctInputsCheckerException`.</span></span> <span data-ttu-id="81d83-113">Zie de API-documentatie op [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="81d83-113">See the API documentation on [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) for more details.</span></span>

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a><span data-ttu-id="81d83-114">De afzonderlijke invoer controle gebruiken in uw C# programma</span><span class="sxs-lookup"><span data-stu-id="81d83-114">Using the Distinct Inputs Checker in your C# Program</span></span>

<span data-ttu-id="81d83-115">Hier volgt een voor beeld van C# een stuur programma code voor het gebruik van de quantum computer Trace Simulator met de `Distinct Inputs Checker` ingeschakeld:</span><span class="sxs-lookup"><span data-stu-id="81d83-115">The following is an example of C# driver code for using the quantum computer trace simulator with the `Distinct Inputs Checker` enabled:</span></span>

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

<span data-ttu-id="81d83-116">De klasse `QCTraceSimulatorConfiguration` slaat de configuratie van de quantum computer Trace Simulator op en kan worden ingesteld als een argument voor de `QCTraceSimulator`-constructor.</span><span class="sxs-lookup"><span data-stu-id="81d83-116">The class `QCTraceSimulatorConfiguration` stores the configuration of the quantum computer trace simulator and can be provided as an argument for the `QCTraceSimulator` constructor.</span></span> <span data-ttu-id="81d83-117">Als `useDistinctInputsChecker` is ingesteld op True, wordt de `Distinct Inputs Checker` ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="81d83-117">When `useDistinctInputsChecker` is set to true the `Distinct Inputs Checker` is enabled.</span></span> <span data-ttu-id="81d83-118">Zie de API-documentatie op [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) en [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="81d83-118">See the API documentation on [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) and [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) for more details.</span></span>

## <a name="see-also"></a><span data-ttu-id="81d83-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="81d83-119">See also</span></span>

- <span data-ttu-id="81d83-120">Het quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) -overzicht.</span><span class="sxs-lookup"><span data-stu-id="81d83-120">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
