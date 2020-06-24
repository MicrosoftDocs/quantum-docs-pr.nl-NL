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
# <a name="distinct-inputs-checker"></a><span data-ttu-id="b1ed3-103">Afzonderlijke invoer controle</span><span class="sxs-lookup"><span data-stu-id="b1ed3-103">Distinct Inputs Checker</span></span>

<span data-ttu-id="b1ed3-104">De `Distinct Inputs Checker` maakt deel uit van de quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span><span class="sxs-lookup"><span data-stu-id="b1ed3-104">The `Distinct Inputs Checker` is a part of the quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="b1ed3-105">Het is ontworpen voor het detecteren van mogelijke fouten in de code.</span><span class="sxs-lookup"><span data-stu-id="b1ed3-105">It is designed for detecting potential bugs in the code.</span></span> <span data-ttu-id="b1ed3-106">Houd rekening met de volgende Q #-code om de problemen te illustreren die door dit pakket worden gedetecteerd:</span><span class="sxs-lookup"><span data-stu-id="b1ed3-106">Consider the following piece of Q# code to illustrate the issues detected by this package:</span></span>

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

<span data-ttu-id="b1ed3-107">Wanneer de gebruiker dit programma bekijkt, wordt ervan uitgegaan dat de volg orde waarin `op1` en `op2` worden aangeroepen, niet van belang is omdat `q1` en `q2` andere qubits en bewerkingen zijn die optreden op verschillende qubits.</span><span class="sxs-lookup"><span data-stu-id="b1ed3-107">When the user looks at this program, they assume that the order in which `op1` and `op2` are called does not matter because `q1` and `q2` are different qubits and operations acting on different qubits commute.</span></span> <span data-ttu-id="b1ed3-108">We gaan nu een voor beeld bekijken waarin deze bewerking wordt gebruikt:</span><span class="sxs-lookup"><span data-stu-id="b1ed3-108">Let us now consider an example, where this operation is used:</span></span>

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

<span data-ttu-id="b1ed3-109">Nu `op1` en `op2` zijn beide verkregen met behulp van gedeeltelijke toepassing en delen ze een Qubit.</span><span class="sxs-lookup"><span data-stu-id="b1ed3-109">Now `op1` and `op2` are both obtained using partial application and share a qubit.</span></span> <span data-ttu-id="b1ed3-110">Wanneer de gebruiker `ApplyBoth` in het bovenstaande voor beeld belt, is het resultaat van de bewerking afhankelijk van de volg orde van `op1` en `op2` in `ApplyBoth` .</span><span class="sxs-lookup"><span data-stu-id="b1ed3-110">When the user calls `ApplyBoth` in the example above the result of the operation will depend on the order of `op1` and `op2` inside `ApplyBoth`.</span></span> <span data-ttu-id="b1ed3-111">Dit is zeker niet wat de gebruiker zou verwachten te doen.</span><span class="sxs-lookup"><span data-stu-id="b1ed3-111">This is definitely not what the user would expect to happen.</span></span> <span data-ttu-id="b1ed3-112">De `Distinct Inputs Checker` detecteert dergelijke situaties wanneer deze zijn ingeschakeld en worden gegenereerd `DistinctInputsCheckerException` .</span><span class="sxs-lookup"><span data-stu-id="b1ed3-112">The `Distinct Inputs Checker` will detect such situations when enabled and will throw `DistinctInputsCheckerException`.</span></span> <span data-ttu-id="b1ed3-113">Zie de API-documentatie op [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b1ed3-113">See the API documentation on [DistinctInputsCheckerException](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException) for more details.</span></span>

## <a name="using-the-distinct-inputs-checker-in-your-c-program"></a><span data-ttu-id="b1ed3-114">De DISTINCT-invoer controle gebruiken in uw C#-programma</span><span class="sxs-lookup"><span data-stu-id="b1ed3-114">Using the Distinct Inputs Checker in your C# Program</span></span>

<span data-ttu-id="b1ed3-115">Hier volgt een voor beeld van een C#-stuur programma voor het gebruik van de quantum computer Trace Simulator met de `Distinct Inputs Checker` ingeschakeld:</span><span class="sxs-lookup"><span data-stu-id="b1ed3-115">The following is an example of C# driver code for using the quantum computer trace simulator with the `Distinct Inputs Checker` enabled:</span></span>

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

<span data-ttu-id="b1ed3-116">De klasse `QCTraceSimulatorConfiguration` slaat de configuratie van de quantum computer Trace Simulator op en kan worden ingesteld als een argument voor de `QCTraceSimulator` constructor.</span><span class="sxs-lookup"><span data-stu-id="b1ed3-116">The class `QCTraceSimulatorConfiguration` stores the configuration of the quantum computer trace simulator and can be provided as an argument for the `QCTraceSimulator` constructor.</span></span> <span data-ttu-id="b1ed3-117">Wanneer `useDistinctInputsChecker` is ingesteld op True, `Distinct Inputs Checker` wordt de is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="b1ed3-117">When `useDistinctInputsChecker` is set to true the `Distinct Inputs Checker` is enabled.</span></span> <span data-ttu-id="b1ed3-118">Zie de API-documentatie op [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) en [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b1ed3-118">See the API documentation on [QCTraceSimulator](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) and [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration?) for more details.</span></span>

## <a name="see-also"></a><span data-ttu-id="b1ed3-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b1ed3-119">See also</span></span>

- <span data-ttu-id="b1ed3-120">Het quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) -overzicht.</span><span class="sxs-lookup"><span data-stu-id="b1ed3-120">The quantum computer [Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
