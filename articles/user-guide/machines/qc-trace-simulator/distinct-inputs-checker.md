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
# <a name="quantum-trace-simulator-distinct-inputs-checker"></a><span data-ttu-id="eca81-103">Quantum Trace Simulator: DISTINCT-invoer controleprogramma</span><span class="sxs-lookup"><span data-stu-id="eca81-103">Quantum trace simulator: distinct inputs checker</span></span>

<span data-ttu-id="eca81-104">De DISTINCT-invoer controle maakt deel uit van de Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span><span class="sxs-lookup"><span data-stu-id="eca81-104">The distinct inputs checker is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="eca81-105">U kunt deze gebruiken voor het detecteren van mogelijke fouten in de code die wordt veroorzaakt door conflicten met gedeelde qubits.</span><span class="sxs-lookup"><span data-stu-id="eca81-105">You can use it to detect potential bugs in the code caused by conflicts with shared qubits.</span></span> 

## <a name="conflicts-with-shared-qubits"></a><span data-ttu-id="eca81-106">Conflicten met gedeelde qubits</span><span class="sxs-lookup"><span data-stu-id="eca81-106">Conflicts with shared qubits</span></span>

<span data-ttu-id="eca81-107">Houd rekening met het volgende stukje Q #-code om de problemen te illustreren die worden gedetecteerd door de afzonderlijke invoer controle:</span><span class="sxs-lookup"><span data-stu-id="eca81-107">Consider the following piece of Q# code to illustrate the issues detected by the distinct inputs checker:</span></span>

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

<span data-ttu-id="eca81-108">Wanneer u dit programma bekijkt, kunt u ervan uitgaan dat de volg orde waarin deze aanroept `op1` en `op2` niet van belang is, omdat `q1` en `q2` andere qubits en bewerkingen op verschillende qubits werken.</span><span class="sxs-lookup"><span data-stu-id="eca81-108">When you look at this program, you can assume that the order in which it calls `op1` and `op2` does not matter, because `q1` and `q2` are different qubits and operations acting on different qubits commute.</span></span> 

<span data-ttu-id="eca81-109">Bekijk nu het volgende voor beeld:</span><span class="sxs-lookup"><span data-stu-id="eca81-109">Now, consider this example:</span></span>

```qsharp
operation ApplyWithNonDistinctInputs() : Unit {
    using (qubits = Qubit[3]) {
        let op1 = CNOT(_, qubits[1]);
        let op2 = CNOT(qubits[1], _);
        ApplyBoth(qubits[0], qubits[2], op1, op2);
    }
}
```

<span data-ttu-id="eca81-110">Houd er rekening mee dat `op1` `op2` beide zijn verkregen met behulp van gedeeltelijke toepassing en een Qubit delen.</span><span class="sxs-lookup"><span data-stu-id="eca81-110">Note that `op1` and `op2` are both obtained using partial application and share a qubit.</span></span> <span data-ttu-id="eca81-111">Wanneer u `ApplyBoth` dit voor beeld aanroept, is het resultaat van de bewerking afhankelijk van de volg orde van `op1` en `op2` binnen `ApplyBoth` -niet wat u verwacht te doen.</span><span class="sxs-lookup"><span data-stu-id="eca81-111">When you call `ApplyBoth` in this example, the result of the operation depends on the order of `op1` and `op2` inside `ApplyBoth` - not what you would expect to happen.</span></span> <span data-ttu-id="eca81-112">Wanneer u de afzonderlijke invoer controle inschakelt, worden dergelijke situaties gedetecteerd en wordt er een gegenereerd `DistinctInputsCheckerException` .</span><span class="sxs-lookup"><span data-stu-id="eca81-112">When you enable the distinct inputs checker, it detects such situations and throws a `DistinctInputsCheckerException`.</span></span> <span data-ttu-id="eca81-113">Zie <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> de Q # API-bibliotheek voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="eca81-113">For more information, see <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> in the Q# API library.</span></span>

## <a name="invoking-the-distinct-inputs-checker"></a><span data-ttu-id="eca81-114">De afzonderlijke invoer controle aanroepen</span><span class="sxs-lookup"><span data-stu-id="eca81-114">Invoking the distinct inputs checker</span></span>

<span data-ttu-id="eca81-115">Als u de Quantum Trace Simulator wilt uitvoeren met de afzonderlijke invoer controle, moet u een <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instantie maken, de `UseDistinctInputsChecker` eigenschap instellen op **True**en vervolgens een nieuw <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> exemplaar maken met `QCTraceSimulatorConfiguration` als de para meter.</span><span class="sxs-lookup"><span data-stu-id="eca81-115">To run the quantum trace simulator with the distinct inputs checker you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UseDistinctInputsChecker` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseDistinctInputsChecker = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-distinct-inputs-checker-in-a-c-host-program"></a><span data-ttu-id="eca81-116">De DISTINCT-invoer controle gebruiken in een C#-hostprogramma</span><span class="sxs-lookup"><span data-stu-id="eca81-116">Using the distinct inputs checker in a C# host program</span></span>

<span data-ttu-id="eca81-117">Hier volgt een voor beeld van een C#-hostprogramma dat gebruikmaakt van de Quantum Trace Simulator, waarbij de afzonderlijke invoer controle is ingeschakeld:</span><span class="sxs-lookup"><span data-stu-id="eca81-117">The following is an example of C# host program that uses the quantum trace simulator with the distinct inputs checker enabled:</span></span>

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

## <a name="see-also"></a><span data-ttu-id="eca81-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="eca81-118">See also</span></span>

- <span data-ttu-id="eca81-119">Het Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Overview (Engelstalig).</span><span class="sxs-lookup"><span data-stu-id="eca81-119">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="eca81-120">De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-verwijzing.</span><span class="sxs-lookup"><span data-stu-id="eca81-120">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="eca81-121">De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-verwijzing.</span><span class="sxs-lookup"><span data-stu-id="eca81-121">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="eca81-122">De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> API-verwijzing.</span><span class="sxs-lookup"><span data-stu-id="eca81-122">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.DistinctInputsCheckerException> API reference.</span></span>
