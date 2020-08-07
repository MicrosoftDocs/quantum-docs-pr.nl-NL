---
title: Resourcetellingen uitvoeren
description: Meer informatie over het verkrijgen van resource schattingen met behulp van een Quantum Trace Simulator.
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.resourcecounts
no-loc:
- Q#
- $$v
ms.openlocfilehash: 35c16e622a390b730ad7385efcc365c212e981fe
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869321"
---
# <a name="obtaining-resource-counts"></a><span data-ttu-id="8a5bd-103">Resourcetellingen uitvoeren</span><span class="sxs-lookup"><span data-stu-id="8a5bd-103">Obtaining resource counts</span></span>

<span data-ttu-id="8a5bd-104">De kosten voor het simuleren van $n $ qubits op klassieke computers worden exponentieel geschaald met $n $.</span><span class="sxs-lookup"><span data-stu-id="8a5bd-104">The cost of simulating $n$ qubits on classical computers scales exponentially with $n$.</span></span> <span data-ttu-id="8a5bd-105">Hiermee wordt de grootte van een quantum chemie-simulatie aanzienlijk beperkt, kunnen we met de volledige status Simulator worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="8a5bd-105">This greatly limits the size of a quantum chemistry simulation we may perform with the full-state simulator.</span></span> <span data-ttu-id="8a5bd-106">Voor grote situaties van schei kunde kunnen we echter nuttige informatie verkrijgen.</span><span class="sxs-lookup"><span data-stu-id="8a5bd-106">For large instances of chemistry, we may nevertheless obtain useful information.</span></span> <span data-ttu-id="8a5bd-107">Hier onderzoeken we hoe resource kosten, zoals het aantal T-poorten of CNOT-poorten, voor het simuleren van schei kunde kunnen worden verkregen op een geautomatiseerde manier met behulp van de [traceer Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span><span class="sxs-lookup"><span data-stu-id="8a5bd-107">Here, we examine how resource costs, such as the number of T-gates or CNOT gates, for simulating chemistry may be obtained in an automated fashion using the [trace simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro).</span></span> <span data-ttu-id="8a5bd-108">Dergelijke informatie informeert ons wanneer quantum computers mogelijk groot genoeg zijn om deze quantum chemie-algoritmen uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="8a5bd-108">Such information informs us of when quantum computers might be large enough to run these quantum chemistry algorithms.</span></span> <span data-ttu-id="8a5bd-109">Zie het gegeven voor beeld voor naslag informatie `GetGateCount` .</span><span class="sxs-lookup"><span data-stu-id="8a5bd-109">For reference, see the provided `GetGateCount` sample.</span></span>

<span data-ttu-id="8a5bd-110">We gaan ervan uit dat we `FermionHamiltonian` van het Broombridge-schema een exemplaar hebben ontvangen zoals beschreven in het voor beeld van het [laden van het bestand](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) .</span><span class="sxs-lookup"><span data-stu-id="8a5bd-110">Let us assume that we already have a `FermionHamiltonian` instance, say, loaded from the Broombridge schema as discussed in the [loading-from-file](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) example.</span></span> 

```csharp
    // Filename of Hamiltonian to be loaded.
    var filename = "...";

    // This deserializes Broombridge.
    var problem = Broombridge.Deserializers.DeserializeBroombridge(filename).ProblemDescriptions.First();

    // This is a data structure representing the Jordan-Wigner encoding 
    // of the Hamiltonian that we may pass to a Q# algorithm.
    var qSharpData = problem.ToQSharpFormat();
```

<span data-ttu-id="8a5bd-111">De syntaxis voor het verkrijgen van resource schattingen is bijna identiek voor het uitvoeren van het algoritme voor de Full-State Simulator.</span><span class="sxs-lookup"><span data-stu-id="8a5bd-111">The syntax for obtaining resource estimates is almost identical to running the algorithm on the full-state simulator.</span></span> <span data-ttu-id="8a5bd-112">We kiezen gewoon een andere doel computer.</span><span class="sxs-lookup"><span data-stu-id="8a5bd-112">We simply choose a different target machine.</span></span> <span data-ttu-id="8a5bd-113">Voor de doel einden van resources is het voldoende om de kosten van één Trotter-stap te evalueren of een Quantum Walk gemaakt door de Qubitization-techniek.</span><span class="sxs-lookup"><span data-stu-id="8a5bd-113">For the purposes of resource estimates, it suffices to evaluate the cost of a single Trotter step, or a quantum walk created by the Qubitization technique.</span></span> <span data-ttu-id="8a5bd-114">De standaard voor het aanroepen van deze algoritmen is als volgt.</span><span class="sxs-lookup"><span data-stu-id="8a5bd-114">The boilerplate for invoking these algorithms is as follows.</span></span>

```qsharp
//////////////////////////////////////////////////////////////////////////
// Using Trotterization //////////////////////////////////////////////////
//////////////////////////////////////////////////////////////////////////

/// # Summary
/// This allocates qubits and applies a single Trotter step.
operation RunTrotterStep (qSharpData: JordanWignerEncodingData) : Unit {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    // We use a Product formula, also known as `Trotterization` to
    // simulate the Hamiltonian.
    // The integrator step size does not affect the gate cost of a single step.
    let trotterStepSize = 1.0;
    
    // Order of integrator
    let trotterOrder = 1;
    let (nQubits, (rescaleFactor, oracle)) = TrotterStepOracle(qSharpData, trotterStepSize, trotterOrder);
    
    // We not allocate qubits an run a single step.
    using (qubits = Qubit[nQubits]) {
        oracle(qubits);
        ResetAll(qubits);
    }
}


//////////////////////////////////////////////////////////////////////////
// Using Qubitization ////////////////////////////////////////////////////
//////////////////////////////////////////////////////////////////////////

/// # Summary
/// This allocates qubits and applies a single qubitization step.
operation RunQubitizationStep (qSharpData: JordanWignerEncodingData) : Double {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    let (nQubits, (l1Norm, oracle)) = QubitizationOracle(qSharpData);
    
    // We now allocate qubits and run a single step.
    using (qubits = Qubit[nQubits]) {
        oracle(qubits);
        ResetAll(qubits);
    }
    
    return l1Norm;
}
```

<span data-ttu-id="8a5bd-115">We configureren nu de trace Simulator voor het bijhouden van de resources waar we geïnteresseerd zijn.</span><span class="sxs-lookup"><span data-stu-id="8a5bd-115">We now configure the trace simulator to track the resources we are interested in.</span></span> <span data-ttu-id="8a5bd-116">In dit geval tellen we primitieve Quantum bewerkingen door de `usePrimitiveOperationsCounter` vlag in te stellen op `true` .</span><span class="sxs-lookup"><span data-stu-id="8a5bd-116">In this case, we count primitive quantum operations by setting the `usePrimitiveOperationsCounter` flag to `true`.</span></span> <span data-ttu-id="8a5bd-117">Er wordt een technisch detail niveau `throwOnUnconstraintMeasurement` ingesteld om `false` uitzonde ringen te voor komen in gevallen waarin de Q# code niet correct wordt bevestigd voor de waarschijnlijkheid van meting resultaten, indien aanwezig.</span><span class="sxs-lookup"><span data-stu-id="8a5bd-117">A technical detail `throwOnUnconstraintMeasurement` is set to `false` to avoid exceptions in cases where the Q# code does not correctly assert of probability of measurement outcomes, if any are performed.</span></span>

```csharp
private static QCTraceSimulator CreateAndConfigureTraceSim()
{
    // Create and configure Trace Simulator
    var config = new QCTraceSimulatorConfiguration()
    {
        usePrimitiveOperationsCounter = true,
        throwOnUnconstraintMeasurement = false
    };

    return new QCTraceSimulator(config);
}
```

<span data-ttu-id="8a5bd-118">We voeren nu de Quantum-algoritme van het stuur programma als volgt uit.</span><span class="sxs-lookup"><span data-stu-id="8a5bd-118">We now run the quantum algorithm from the driver program as follows.</span></span>

```csharp
// Instantiate a trace simulator instance
QCTraceSimulator sim = CreateAndConfigureTraceSim();

// Run the quantum algorithm on the trace simulator.
RunQubitizationStep.Run(sim, qSharpData);

// Print all resource counts to file.
var gateStats = sim.ToCSV();
foreach (var x in gateStats)
{
    System.IO.File.WriteAllLines($"QubitizationGateCountEstimates.{x.Key}.csv", new string[] { x.Value });
}
```