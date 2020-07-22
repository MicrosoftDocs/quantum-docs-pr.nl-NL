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
# <a name="quantum-trace-simulator-invalidated-qubits-use-checker"></a><span data-ttu-id="e059c-103">Quantum Trace Simulator: ongeldig qubits use Checker</span><span class="sxs-lookup"><span data-stu-id="e059c-103">Quantum trace simulator: invalidated qubits use checker</span></span>

<span data-ttu-id="e059c-104">De ongeldig qubits use-controle is een onderdeel van de Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span><span class="sxs-lookup"><span data-stu-id="e059c-104">The invalidated qubits use checker is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="e059c-105">U kunt dit gebruiken om mogelijke fouten te detecteren in de code die is veroorzaakt door ongeldige qubits.</span><span class="sxs-lookup"><span data-stu-id="e059c-105">You can use it to detect potential bugs in the code caused by invalid qubits.</span></span> 

## <a name="invalid-qubits"></a><span data-ttu-id="e059c-106">Ongeldige qubits</span><span class="sxs-lookup"><span data-stu-id="e059c-106">Invalid qubits</span></span>

<span data-ttu-id="e059c-107">Houd rekening met het volgende deel van Q # code voor het illustreren van de problemen die worden gedetecteerd door de ongeldig qubits-controle functie:</span><span class="sxs-lookup"><span data-stu-id="e059c-107">Consider the following piece of Q# code to illustrate the issues detected by the invalidated qubits use checker:</span></span>

```qsharp
operation UseReleasedQubit() : Unit {
    mutable q = new Qubit[1];
    using (ans = Qubit()) {
        set q w/= 0 <- ans;
    }
    H(q[0]);
}
```

<span data-ttu-id="e059c-108">Wanneer u de `H` bewerking toepast op `q[0]` , wijst deze naar een reeds vrijgegeven Qubit. Dit kan leiden tot ongedefinieerd gedrag.</span><span class="sxs-lookup"><span data-stu-id="e059c-108">When you apply the `H` operation to `q[0]`, it points to an already released qubit, which can cause undefined behavior.</span></span> <span data-ttu-id="e059c-109">Wanneer de ongeldig qubits-controle functie is ingeschakeld, wordt de uitzonde ring gegenereerd `InvalidatedQubitsUseCheckerException` als een bewerking wordt toegepast op een reeds vrijgegeven Qubit.</span><span class="sxs-lookup"><span data-stu-id="e059c-109">When the Invalidated Qubits Use Checker is enabled, it throws the exception `InvalidatedQubitsUseCheckerException` if the program applies an operation to an already released qubit.</span></span> <span data-ttu-id="e059c-110">Voor meer informatie raadpleegt u <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException>.</span><span class="sxs-lookup"><span data-stu-id="e059c-110">For more information, see <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException>.</span></span>

## <a name="invoking-the-invalidated-qubits-use-checker"></a><span data-ttu-id="e059c-111">Het aanroepen van de ongeldig te controleren qubits use Checker</span><span class="sxs-lookup"><span data-stu-id="e059c-111">Invoking the invalidated qubits use checker</span></span>

<span data-ttu-id="e059c-112">Als u de Quantum Trace Simulator wilt uitvoeren met de ongeldig qubits use-controle, moet u een <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instantie maken, de `UseInvalidatedQubitsUseChecker` eigenschap instellen op **True**en vervolgens een nieuw <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> exemplaar maken met `QCTraceSimulatorConfiguration` als de para meter.</span><span class="sxs-lookup"><span data-stu-id="e059c-112">To run the quantum trace simulator with the invalidated qubits use checker you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UseInvalidatedQubitsUseChecker` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseInvalidatedQubitsUseChecker = true;
var sim = new QCTraceSimulator(config);
```


## <a name="using-the-invalidated-qubits-use-checker-in-a-c-host-program"></a><span data-ttu-id="e059c-113">De ongeldig qubits use Checker gebruiken in een C#-hostprogramma</span><span class="sxs-lookup"><span data-stu-id="e059c-113">Using the invalidated qubits use checker in a C# host program</span></span>

<span data-ttu-id="e059c-114">Hier volgt een voor beeld van C#-hostgroepen die gebruikmaken van de Quantum Trace Simulator waarbij de ongeldig qubits use-controle is ingeschakeld:</span><span class="sxs-lookup"><span data-stu-id="e059c-114">The following is an example of C# host programs that uses the quantum trace simulator with the invalidated qubits use checker enabled:</span></span> 

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

## <a name="see-also"></a><span data-ttu-id="e059c-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e059c-115">See also</span></span>

- <span data-ttu-id="e059c-116">Het Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Overview (Engelstalig).</span><span class="sxs-lookup"><span data-stu-id="e059c-116">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="e059c-117">De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-verwijzing.</span><span class="sxs-lookup"><span data-stu-id="e059c-117">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="e059c-118">De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-verwijzing.</span><span class="sxs-lookup"><span data-stu-id="e059c-118">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="e059c-119">De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException> API-verwijzing.</span><span class="sxs-lookup"><span data-stu-id="e059c-119">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.InvalidatedQubitsUseCheckerException> API reference.</span></span>