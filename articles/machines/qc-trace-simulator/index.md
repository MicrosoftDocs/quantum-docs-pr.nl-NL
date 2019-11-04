---
title: Kwantumcomputer-traceersimulator | Microsoft Docs
description: Overzicht van kwantumcomputer-traceersimulator
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
ms.openlocfilehash: 7fd9d1fa4fb3c5dd216d846038abd40454ece2e8
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2019
ms.locfileid: "73035126"
---
# <a name="quantum-trace-simulator"></a><span data-ttu-id="e8e7a-103">Kwantumtraceersimulator</span><span class="sxs-lookup"><span data-stu-id="e8e7a-103">Quantum Trace Simulator</span></span>

<span data-ttu-id="e8e7a-104">De kwantumcomputer-traceersimulator voert een kwantumprogramma uit zonder de toestand van een kwantumcomputer daadwerkelijk te simuleren.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-104">The Microsoft quantum computer trace simulator executes a quantum program without actually simulating the state of a quantum computer.</span></span>  <span data-ttu-id="e8e7a-105">Daarom kunnen met de traceersimulator kwantumprogramma's van duizenden qubits worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-105">For this reason, the trace simulator can execute quantum programs that use thousands of qubits.</span></span>  <span data-ttu-id="e8e7a-106">De simulator is handig voor twee hoofddoelen:</span><span class="sxs-lookup"><span data-stu-id="e8e7a-106">It is useful for two main purposes:</span></span> 

* <span data-ttu-id="e8e7a-107">Het opsporen van fouten in klassieke code die deel uitmaakt van een kwantumprogramma.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-107">Debugging classical code that is part of a quantum program.</span></span> 
* <span data-ttu-id="e8e7a-108">Het schatten van de benodigde resources voor het uitvoeren van een bepaald exemplaar van een kwantumprogramma op een kwantumcomputer.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-108">Estimating the resources required to run a given instance of a quantum program on a quantum computer.</span></span>

<span data-ttu-id="e8e7a-109">De traceersimulator is afhankelijk van aanvullende gegevens die door de gebruiker worden verstrekt wanneer er metingen moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-109">The trace simulator relies on additional information provided by the user when measurements must be performed.</span></span> <span data-ttu-id="e8e7a-110">Zie de sectie [De waarschijnlijkheid van metingsresultaten opgeven](#providing-the-probability-of-measurement-outcomes) voor meer informatie hierover.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-110">See Section [Providing the probability of measurement outcomes](#providing-the-probability-of-measurement-outcomes) for more details on this.</span></span> 

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="e8e7a-111">De waarschijnlijkheid van metingsresultaten opgeven</span><span class="sxs-lookup"><span data-stu-id="e8e7a-111">Providing the Probability of Measurement Outcomes</span></span>

<span data-ttu-id="e8e7a-112">Er zijn twee soorten metingen die voorkomen in kwantumalgoritmen.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-112">There are two kinds of measurements that appear in quantum algorithms.</span></span> <span data-ttu-id="e8e7a-113">De eerste soort speelt een ondersteunende rol waarbij de gebruiker de waarschijnlijkheid van de resultaten doorgaans kent.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-113">The first kind plays an auxiliary role where the user usually knows the probability of the outcomes.</span></span> <span data-ttu-id="e8e7a-114">In dit geval kan de gebruiker <xref:microsoft.quantum.primitive.assertprob> schrijven vanuit de naamruimte <xref:microsoft.quantum.primitive> om deze kennis uit te drukken.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-114">In this case the user can write <xref:microsoft.quantum.primitive.assertprob> from the <xref:microsoft.quantum.primitive> namespace to express this knowledge.</span></span> <span data-ttu-id="e8e7a-115">Het volgende voorbeeld illustreert dit:</span><span class="sxs-lookup"><span data-stu-id="e8e7a-115">The following example illustrates this:</span></span>

```qsharp
operation Teleportation (source : Qubit, target : Qubit) : Unit {

    using (ancilla = Qubit()) {

        H(ancilla);
        CNOT(ancilla, target);

        CNOT(source, ancilla);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [ancilla], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(ancilla) == One) { X(target); X(ancilla); }
    }
}
```

<span data-ttu-id="e8e7a-116">Wanneer `AssertProb` wordt uitgevoerd met de traceersimulator, wordt vastgelegd dat aan meting `PauliZ` op `source` en `ancilla` een resultaat van `Zero` met een waarschijnlijkheid van 0,5 moet worden toegekend.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-116">When the trace simulator executes `AssertProb` it will record that measuring `PauliZ` on `source` and `ancilla` should be given an outcome of `Zero` with probability 0.5.</span></span> <span data-ttu-id="e8e7a-117">Wanneer later `M` wordt uitgevoerd, worden de vastgelegde waarden van de waarschijnlijkheid van de resultaten gevonden en wordt voor `M` een resultaat van `Zero` of `One` geretourneerd met een waarschijnlijkheid van 0,5.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-117">When the simulator executes `M` later, it will find the recorded values of the outcome probabilities and `M` will return `Zero` or `One` with probability 0.5.</span></span> <span data-ttu-id="e8e7a-118">Wanneer dezelfde code wordt uitgevoerd in een simulator die de kwantumtoestand bijhoudt, wordt in die simulator gecontroleerd of de in `AssertProb` opgegeven waarschijnlijkheden juist zijn.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-118">When the same code is executed on a simulator that keeps track of the quantum state, such a simulator will check that the provided probabilities in `AssertProb` are correct.</span></span>

## <a name="running-your-program-with-the-quantum-computer-trace-simulator"></a><span data-ttu-id="e8e7a-119">Uw programma uitvoeren met de kwantumcomputertraceersimulator</span><span class="sxs-lookup"><span data-stu-id="e8e7a-119">Running your Program with the Quantum Computer Trace Simulator</span></span> 

<span data-ttu-id="e8e7a-120">De kwantumcomputertraceersimulator kan in feite gewoon worden gezien als een andere doelcomputer.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-120">The quantum computer trace simulator may be viewed as just another target machine.</span></span> <span data-ttu-id="e8e7a-121">Het C#-stuurprogramma voor het gebruik ervan lijkt veel op dat van elke willekeurige andere kwantumsimulator:</span><span class="sxs-lookup"><span data-stu-id="e8e7a-121">The C# driver program for using it is very similar to the one for any other quantum Simulator:</span></span> 

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
            QCTraceSimulator sim = new QCTraceSimulator();
            var res = MyQuantumProgram.Run().Result;
            System.Console.WriteLine("Press any key to continue...");
            System.Console.ReadKey();
        }
    }
}
```

<span data-ttu-id="e8e7a-122">Als een of meer metingen niet zijn geannoteerd met behulp van `AssertProb`, wordt door de simulator een `UnconstrainedMeasurementException`-uitzondering van de naamruimte `Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators` geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-122">Note that if there is at least one measurement not annotated using `AssertProb`, the simulator will throw `UnconstrainedMeasurementException` from the `Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators` namespace.</span></span> <span data-ttu-id="e8e7a-123">Zie de API-documentatie over [UnconstrainedMeasurementException](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.UnconstrainedMeasurementException) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-123">See the API documentation on [UnconstrainedMeasurementException](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.UnconstrainedMeasurementException) for more details.</span></span>

<span data-ttu-id="e8e7a-124">Naast het onderdeel voor het uitvoeren van kwantumprogramma's bevat de traceersimulator vijf onderdelen voor het opsporen van fouten in programma's en het schatten van de benodigde resources voor kwantumprogramma's:</span><span class="sxs-lookup"><span data-stu-id="e8e7a-124">In addition to running quantum programs, the trace simulator comes with five components for detecting bugs in programs and performing quantum program resource estimates:</span></span> 

* [<span data-ttu-id="e8e7a-125">Controle op verschillende input</span><span class="sxs-lookup"><span data-stu-id="e8e7a-125">Distinct Inputs Checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs)
* [<span data-ttu-id="e8e7a-126">Controle op gebruik van ongeldige qubits</span><span class="sxs-lookup"><span data-stu-id="e8e7a-126">Invalidated Qubits Use Checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)
* [<span data-ttu-id="e8e7a-127">Teller primitieve bewerkingen</span><span class="sxs-lookup"><span data-stu-id="e8e7a-127">Primitive Operations Counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)
* [<span data-ttu-id="e8e7a-128">Teller circuitdiepte</span><span class="sxs-lookup"><span data-stu-id="e8e7a-128">Circuit Depth Counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)
* [<span data-ttu-id="e8e7a-129">Teller circuitbreedte</span><span class="sxs-lookup"><span data-stu-id="e8e7a-129">Circuit Width Counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)

<span data-ttu-id="e8e7a-130">Elk van deze onderdelen kan worden ingeschakeld door de juiste vlaggen in te stellen in `QCTraceSimulatorConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-130">Each of these components may be enabled by setting appropriate flags in `QCTraceSimulatorConfiguration`.</span></span> <span data-ttu-id="e8e7a-131">Meer informatie over het gebruik van elk van deze onderdelen vindt u in de bijbehorende referentiebestanden.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-131">More details about using each of these components are provided in the corresponding reference files.</span></span> <span data-ttu-id="e8e7a-132">Zie de API-documentatie over [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) voor specifieke informatie.</span><span class="sxs-lookup"><span data-stu-id="e8e7a-132">See the API documentation on [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) for specific details.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8e7a-133">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e8e7a-133">See also</span></span>
<span data-ttu-id="e8e7a-134">Naslaginformatie over de kwantumcomputer-[traceersimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) voor C#</span><span class="sxs-lookup"><span data-stu-id="e8e7a-134">The quantum computer [trace simulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) C# reference</span></span> 

