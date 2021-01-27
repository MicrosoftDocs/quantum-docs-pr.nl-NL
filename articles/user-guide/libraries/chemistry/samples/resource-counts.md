---
title: Resourcetellingen uitvoeren
description: Meer informatie over het verkrijgen van resource schattingen met behulp van een Quantum Trace Simulator.
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: sample
uid: microsoft.quantum.chemistry.examples.resourcecounts
no-loc:
- Q#
- $$v
ms.openlocfilehash: b8974114a5629fa1928b5774e79aba93fa3d1f7d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856243"
---
# <a name="obtaining-resource-counts"></a>Resourcetellingen uitvoeren

De kosten voor het simuleren van $n $ qubits op klassieke computers worden exponentieel geschaald met $n $. Hiermee wordt de grootte van een quantum chemie-simulatie aanzienlijk beperkt, kunnen we met de volledige status Simulator worden uitgevoerd. Voor grote situaties van schei kunde kunnen we echter nuttige informatie verkrijgen. Hier onderzoeken we hoe resource kosten, zoals het aantal T-poorten of CNOT-poorten, voor het simuleren van schei kunde kunnen worden verkregen op een geautomatiseerde manier met behulp van de [traceer Simulator](xref:microsoft.quantum.machines.qc-trace-simulator.intro). Dergelijke informatie informeert ons wanneer quantum computers mogelijk groot genoeg zijn om deze quantum chemie-algoritmen uit te voeren. Zie het gegeven voor beeld voor naslag informatie `GetGateCount` .

We gaan ervan uit dat we `FermionHamiltonian` van het Broombridge-schema een exemplaar hebben ontvangen zoals beschreven in het voor beeld van het [laden van het bestand](xref:microsoft.quantum.chemistry.examples.loadhamiltonian) . 

```csharp
    // Filename of Hamiltonian to be loaded.
    var filename = "...";

    // This deserializes Broombridge.
    var problem = Broombridge.Deserializers.DeserializeBroombridge(filename).ProblemDescriptions.First();

    // This is a data structure representing the Jordan-Wigner encoding 
    // of the Hamiltonian that we may pass to a Q# algorithm.
    var qSharpData = problem.ToQSharpFormat();
```

De syntaxis voor het verkrijgen van resource schattingen is bijna identiek voor het uitvoeren van het algoritme voor de Full-State Simulator. We kiezen gewoon een andere doel computer. Voor de doel einden van resources is het voldoende om de kosten van één Trotter-stap te evalueren of een Quantum Walk gemaakt door de Qubitization-techniek. De standaard voor het aanroepen van deze algoritmen is als volgt.

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

We configureren nu de trace Simulator voor het bijhouden van de resources waar we geïnteresseerd zijn. In dit geval tellen we primitieve Quantum bewerkingen door de `usePrimitiveOperationsCounter` vlag in te stellen op `true` . Er wordt een technisch detail niveau `throwOnUnconstraintMeasurement` ingesteld om `false` uitzonde ringen te voor komen in gevallen waarin de Q# code niet correct wordt bevestigd voor de waarschijnlijkheid van meting resultaten, indien aanwezig.

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

We voeren nu de Quantum-algoritme van het stuur programma als volgt uit.

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