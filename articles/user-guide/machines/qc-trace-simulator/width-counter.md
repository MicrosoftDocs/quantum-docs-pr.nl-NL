---
title: Counter-Quantum Development Kit
description: Meer informatie over de micro soft QDK width Counter, die gebruikmaakt van de Quantum Trace Simulator voor het tellen van het aantal qubits dat is toegewezen en uitgeleend door bewerkingen in een Q# programma.
author: vadym-kl
ms.author: vadym@microsoft.com
ms.date: 06/25/2020
ms.topic: article
uid: microsoft.quantum.machines.qc-trace-simulator.width-counter
no-loc:
- Q#
- $$v
ms.openlocfilehash: 02f4937aaccf7bf49d6450355c6b42b273071b2e
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87868199"
---
# <a name="quantum-trace-simulator-width-counter"></a><span data-ttu-id="ea08e-103">Quantum Trace Simulator: breedte teller</span><span class="sxs-lookup"><span data-stu-id="ea08e-103">Quantum trace simulator: width counter</span></span>

<span data-ttu-id="ea08e-104">De teller voor de breedte is een onderdeel van de Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span><span class="sxs-lookup"><span data-stu-id="ea08e-104">The width counter is a part of the Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="ea08e-105">U kunt deze gebruiken om het aantal toegewezen qubits te tellen dat door elke bewerking in een programma wordt verdeeld en uitgeleend Q# .</span><span class="sxs-lookup"><span data-stu-id="ea08e-105">You can use it to count the number of qubits allocated and borrowed by each operation in a Q# program.</span></span> <span data-ttu-id="ea08e-106">Met sommige primitieve bewerkingen kunt u extra qubits toewijzen, bijvoorbeeld gecontroleerde `X` bewerkingen of beheerde `T` bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="ea08e-106">Some primitive operations can allocate extra qubits, for example, multiply controlled `X` operations or controlled `T` operations.</span></span>

## <a name="invoking-the-width-counter"></a><span data-ttu-id="ea08e-107">Aanroepen van de teller voor breedte</span><span class="sxs-lookup"><span data-stu-id="ea08e-107">Invoking the width counter</span></span>

<span data-ttu-id="ea08e-108">Als u de Quantum Trace Simulator met de breedte teller wilt uitvoeren, moet u een <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> exemplaar maken, de `UseWidthCounter` eigenschap instellen op **True**en vervolgens een nieuw <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> exemplaar maken met de `QCTraceSimulatorConfiguration` as-para meter.</span><span class="sxs-lookup"><span data-stu-id="ea08e-108">To run the quantum trace simulator with the width counter, you must create a <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> instance, set the `UseWidthCounter` property to **true**, and then create a new <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> instance with the `QCTraceSimulatorConfiguration` as the parameter.</span></span> 

```csharp
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
var sim = new QCTraceSimulator(config);
```

## <a name="using-the-width-counter-in-a-c-host-program"></a><span data-ttu-id="ea08e-109">De teller width gebruiken in een C#-hostprogramma</span><span class="sxs-lookup"><span data-stu-id="ea08e-109">Using the width counter in a C# host program</span></span>

<span data-ttu-id="ea08e-110">In het C#-voor beeld dat volgt in deze sectie wordt het aantal extra qubits berekend dat wordt toegewezen door de implementatie van een door vermenigvuldiging beheerde <xref:microsoft.quantum.intrinsic.x> bewerking, op basis van de volgende Q# voorbeeld code:</span><span class="sxs-lookup"><span data-stu-id="ea08e-110">The C# example that follows in this section computes the number of extra qubits allocated by the implementation of a multiply controlled <xref:microsoft.quantum.intrinsic.x> operation, based on the following Q# sample code:</span></span>

```qsharp
open Microsoft.Quantum.Intrinsic;
open Microsoft.Quantum.Arrays;
operation ApplyMultiControlledX( numberOfQubits : Int ) : Unit {
    using(qubits = Qubit[numberOfQubits]) {
        Controlled X (Rest(qubits), Head(qubits));
    } 
}
```

<span data-ttu-id="ea08e-111">Met de bewerking vermenigvuldigen <xref:microsoft.quantum.intrinsic.x> wordt een totaal van vijf qubits toegepast, worden er twee [bijkomende qubits](xref:microsoft.quantum.glossary#ancilla)toegewezen, en heeft dit een invoer breedte van **5**.</span><span class="sxs-lookup"><span data-stu-id="ea08e-111">The multiply controlled <xref:microsoft.quantum.intrinsic.x> operation acts on a total of five qubits, allocates two [ancillary qubits](xref:microsoft.quantum.glossary#ancilla), and has an input width of **5**.</span></span> <span data-ttu-id="ea08e-112">Gebruik het volgende C#-programma om de aantallen te controleren:</span><span class="sxs-lookup"><span data-stu-id="ea08e-112">Use the following C# program to verify the counts:</span></span>

```csharp 
var config = new QCTraceSimulatorConfiguration();
config.UseWidthCounter = true;
var sim = new QCTraceSimulator(config);
int totalNumberOfQubits = 5;
var res = ApplyMultiControlledX.Run(sim, totalNumberOfQubits).Result;

double allocatedQubits = 
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.ExtraWidth,
        functor: OperationFunctor.Controlled); 

double inputWidth =
    sim.GetMetric<Primitive.X, ApplyMultiControlledX>(
        WidthCounter.Metrics.InputWidth,
        functor: OperationFunctor.Controlled);
```

<span data-ttu-id="ea08e-113">Het eerste deel van het programma voert de `ApplyMultiControlledX` bewerking uit.</span><span class="sxs-lookup"><span data-stu-id="ea08e-113">The first part of the program runs the `ApplyMultiControlledX` operation.</span></span> <span data-ttu-id="ea08e-114">In het tweede deel wordt de [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) methode gebruikt om het aantal toegewezen qubits op te halen, evenals het aantal qubits dat de `Controlled X` bewerking heeft ontvangen als invoer.</span><span class="sxs-lookup"><span data-stu-id="ea08e-114">The second part uses the [`QCTraceSimulator.GetMetric`](https://docs.microsoft.com/dotnet/api/microsoft.quantum.simulation.simulators.qctracesimulators.qctracesimulator.getmetric) method to retrieve the number of allocated qubits as well as the number of qubits that the `Controlled X` operation received as input.</span></span> 

<span data-ttu-id="ea08e-115">Ten slotte kunt u alle statistieken die worden verzameld door de teller breedte in CSV-indeling uitvoeren met het volgende:</span><span class="sxs-lookup"><span data-stu-id="ea08e-115">Finally, you can output all the statistics collected by the width counter in CSV format using the following:</span></span>
```csharp
string csvSummary = sim.ToCSV()[MetricsCountersNames.widthCounter];
```

## <a name="see-also"></a><span data-ttu-id="ea08e-116">Zie tevens</span><span class="sxs-lookup"><span data-stu-id="ea08e-116">See also</span></span>

- <span data-ttu-id="ea08e-117">Het Quantum Development Kit [Quantum Trace Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) Overview (Engelstalig).</span><span class="sxs-lookup"><span data-stu-id="ea08e-117">The Quantum Development Kit [Quantum trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro) overview.</span></span>
- <span data-ttu-id="ea08e-118">De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API-verwijzing.</span><span class="sxs-lookup"><span data-stu-id="ea08e-118">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulator> API reference.</span></span>
- <span data-ttu-id="ea08e-119">De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API-verwijzing.</span><span class="sxs-lookup"><span data-stu-id="ea08e-119">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.QCTraceSimulatorConfiguration> API reference.</span></span>
- <span data-ttu-id="ea08e-120">De <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.WidthCounter> API-verwijzing.</span><span class="sxs-lookup"><span data-stu-id="ea08e-120">The <xref:Microsoft.Quantum.Simulation.Simulators.QCTraceSimulators.MetricsNames.WidthCounter> API reference.</span></span>
