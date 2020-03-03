---
title: Trajectsimulator kwantumcomputer
description: Meer informatie over hoe u de Microsoft Quantum-computertracesimulator kunt gebruiken om fouten in klassieke code op te sporen en om resourcevereisten van een kwantumprogramma in te schatten.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 12/11/2017
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.intro
ms.openlocfilehash: 72c259933d2df8f79319e6c0c65ae181a9f9cff3
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77906080"
---
# <a name="quantum-trace-simulator"></a><span data-ttu-id="1fced-103">Kwantumtraceersimulator</span><span class="sxs-lookup"><span data-stu-id="1fced-103">Quantum Trace Simulator</span></span>

<span data-ttu-id="1fced-104">De kwantumcomputer-traceersimulator voert een kwantumprogramma uit zonder de toestand van een kwantumcomputer daadwerkelijk te simuleren.</span><span class="sxs-lookup"><span data-stu-id="1fced-104">The Microsoft quantum computer trace simulator executes a quantum program without actually simulating the state of a quantum computer.</span></span>  <span data-ttu-id="1fced-105">Daarom kunnen met de traceersimulator kwantumprogramma's van duizenden qubits worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="1fced-105">For this reason, the trace simulator can execute quantum programs that use thousands of qubits.</span></span>  <span data-ttu-id="1fced-106">De simulator is handig voor twee hoofddoelen:</span><span class="sxs-lookup"><span data-stu-id="1fced-106">It is useful for two main purposes:</span></span> 

* <span data-ttu-id="1fced-107">Het opsporen van fouten in klassieke code die deel uitmaakt van een kwantumprogramma.</span><span class="sxs-lookup"><span data-stu-id="1fced-107">Debugging classical code that is part of a quantum program.</span></span> 
* <span data-ttu-id="1fced-108">Het schatten van de benodigde resources voor het uitvoeren van een bepaald exemplaar van een kwantumprogramma op een kwantumcomputer.</span><span class="sxs-lookup"><span data-stu-id="1fced-108">Estimating the resources required to run a given instance of a quantum program on a quantum computer.</span></span>

<span data-ttu-id="1fced-109">De traceersimulator is afhankelijk van aanvullende gegevens die door de gebruiker worden verstrekt wanneer er metingen moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="1fced-109">The trace simulator relies on additional information provided by the user when measurements must be performed.</span></span> <span data-ttu-id="1fced-110">Zie de sectie [De waarschijnlijkheid van metingsresultaten opgeven](#providing-the-probability-of-measurement-outcomes) voor meer informatie hierover.</span><span class="sxs-lookup"><span data-stu-id="1fced-110">See Section [Providing the probability of measurement outcomes](#providing-the-probability-of-measurement-outcomes) for more details on this.</span></span> 

## <a name="providing-the-probability-of-measurement-outcomes"></a><span data-ttu-id="1fced-111">De waarschijnlijkheid van metingsresultaten opgeven</span><span class="sxs-lookup"><span data-stu-id="1fced-111">Providing the Probability of Measurement Outcomes</span></span>

<span data-ttu-id="1fced-112">Er zijn twee soorten metingen die voorkomen in kwantumalgoritmen.</span><span class="sxs-lookup"><span data-stu-id="1fced-112">There are two kinds of measurements that appear in quantum algorithms.</span></span> <span data-ttu-id="1fced-113">De eerste soort speelt een ondersteunende rol waarbij de gebruiker de waarschijnlijkheid van de resultaten doorgaans kent.</span><span class="sxs-lookup"><span data-stu-id="1fced-113">The first kind plays an auxiliary role where the user usually knows the probability of the outcomes.</span></span> <span data-ttu-id="1fced-114">In dit geval kan de gebruiker <xref:microsoft.quantum.intrinsic.assertprob> schrijven vanuit de naamruimte <xref:microsoft.quantum.intrinsic> om deze kennis uit te drukken.</span><span class="sxs-lookup"><span data-stu-id="1fced-114">In this case the user can write <xref:microsoft.quantum.intrinsic.assertprob> from the <xref:microsoft.quantum.intrinsic> namespace to express this knowledge.</span></span> <span data-ttu-id="1fced-115">Het volgende voorbeeld illustreert dit:</span><span class="sxs-lookup"><span data-stu-id="1fced-115">The following example illustrates this:</span></span>

```qsharp
operation TeleportQubit(source : Qubit, target : Qubit) : Unit {
    using (qubit = Qubit()) {
        H(qubit);
        CNOT(qubit, target);
        CNOT(source, qubit);
        H(source);

        AssertProb([PauliZ], [source], Zero, 0.5, "Outcomes must be equally likely", 1e-5);
        AssertProb([PauliZ], [q], Zero, 0.5, "Outcomes must be equally likely", 1e-5);

        if (M(source) == One)  { Z(target); X(source); }
        if (M(q) == One) { X(target); X(q); }
    }
}
```

<span data-ttu-id="1fced-116">Wanneer `AssertProb` wordt uitgevoerd met de traceersimulator, wordt vastgelegd dat aan meting `PauliZ` op `source` en `q` een resultaat van `Zero` met een waarschijnlijkheid van 0,5 moet worden toegekend.</span><span class="sxs-lookup"><span data-stu-id="1fced-116">When the trace simulator executes `AssertProb` it will record that measuring `PauliZ` on `source` and `q` should be given an outcome of `Zero` with probability 0.5.</span></span> <span data-ttu-id="1fced-117">Wanneer later `M` wordt uitgevoerd, worden de vastgelegde waarden van de waarschijnlijkheid van de resultaten gevonden en wordt voor `M` een resultaat van `Zero` of `One` geretourneerd met een waarschijnlijkheid van 0,5.</span><span class="sxs-lookup"><span data-stu-id="1fced-117">When the simulator executes `M` later, it will find the recorded values of the outcome probabilities and `M` will return `Zero` or `One` with probability 0.5.</span></span> <span data-ttu-id="1fced-118">Wanneer dezelfde code wordt uitgevoerd in een simulator die de kwantumtoestand bijhoudt, wordt in die simulator gecontroleerd of de in `AssertProb` opgegeven waarschijnlijkheden juist zijn.</span><span class="sxs-lookup"><span data-stu-id="1fced-118">When the same code is executed on a simulator that keeps track of the quantum state, such a simulator will check that the provided probabilities in `AssertProb` are correct.</span></span>

## <a name="running-your-program-with-the-quantum-computer-trace-simulator"></a><span data-ttu-id="1fced-119">Uw programma uitvoeren met de kwantumcomputertraceersimulator</span><span class="sxs-lookup"><span data-stu-id="1fced-119">Running your Program with the Quantum Computer Trace Simulator</span></span> 

<span data-ttu-id="1fced-120">De kwantumcomputertraceersimulator kan in feite gewoon worden gezien als een andere doelcomputer.</span><span class="sxs-lookup"><span data-stu-id="1fced-120">The quantum computer trace simulator may be viewed as just another target machine.</span></span> <span data-ttu-id="1fced-121">Het C#-stuurprogramma voor het gebruik ervan lijkt veel op dat van elke willekeurige andere kwantumsimulator:</span><span class="sxs-lookup"><span data-stu-id="1fced-121">The C# driver program for using it is very similar to the one for any other quantum Simulator:</span></span> 

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

<span data-ttu-id="1fced-122">Als een of meer metingen niet zijn geannoteerd met behulp van `AssertProb`, wordt door de simulator een `UnconstrainedMeasurementException`-uitzondering van de naamruimte `Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators` geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="1fced-122">Note that if there is at least one measurement not annotated using `AssertProb`, the simulator will throw `UnconstrainedMeasurementException` from the `Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators` namespace.</span></span> <span data-ttu-id="1fced-123">Zie de API-documentatie over [UnconstrainedMeasurementException](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.UnconstrainedMeasurementException) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1fced-123">See the API documentation on [UnconstrainedMeasurementException](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.UnconstrainedMeasurementException) for more details.</span></span>

<span data-ttu-id="1fced-124">Naast het onderdeel voor het uitvoeren van kwantumprogramma's bevat de traceersimulator vijf onderdelen voor het opsporen van fouten in programma's en het schatten van de benodigde resources voor kwantumprogramma's:</span><span class="sxs-lookup"><span data-stu-id="1fced-124">In addition to running quantum programs, the trace simulator comes with five components for detecting bugs in programs and performing quantum program resource estimates:</span></span> 

* [<span data-ttu-id="1fced-125">Controle op verschillende input</span><span class="sxs-lookup"><span data-stu-id="1fced-125">Distinct Inputs Checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.distinct-inputs)
* [<span data-ttu-id="1fced-126">Controle op gebruik van ongeldige qubits</span><span class="sxs-lookup"><span data-stu-id="1fced-126">Invalidated Qubits Use Checker</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.invalidated-qubits)
* [<span data-ttu-id="1fced-127">Teller primitieve bewerkingen</span><span class="sxs-lookup"><span data-stu-id="1fced-127">Primitive Operations Counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.primitive-counter)
* [<span data-ttu-id="1fced-128">Teller circuitdiepte</span><span class="sxs-lookup"><span data-stu-id="1fced-128">Circuit Depth Counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.depth-counter)
* [<span data-ttu-id="1fced-129">Teller circuitbreedte</span><span class="sxs-lookup"><span data-stu-id="1fced-129">Circuit Width Counter</span></span>](xref:microsoft.quantum.machines.qc-trace-simulator.width-counter)

<span data-ttu-id="1fced-130">Elk van deze onderdelen kan worden ingeschakeld door de juiste vlaggen in te stellen in `QCTraceSimulatorConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="1fced-130">Each of these components may be enabled by setting appropriate flags in `QCTraceSimulatorConfiguration`.</span></span> <span data-ttu-id="1fced-131">Meer informatie over het gebruik van elk van deze onderdelen vindt u in de bijbehorende referentiebestanden.</span><span class="sxs-lookup"><span data-stu-id="1fced-131">More details about using each of these components are provided in the corresponding reference files.</span></span> <span data-ttu-id="1fced-132">Zie de API-documentatie over [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) voor specifieke informatie.</span><span class="sxs-lookup"><span data-stu-id="1fced-132">See the API documentation on [QCTraceSimulatorConfiguration](https://docs.microsoft.com/dotnet/api/Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration) for specific details.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fced-133">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1fced-133">See also</span></span>
<span data-ttu-id="1fced-134">Naslaginformatie over de kwantumcomputer-[traceersimulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) voor C#</span><span class="sxs-lookup"><span data-stu-id="1fced-134">The quantum computer [trace simulator](xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator) C# reference</span></span> 

