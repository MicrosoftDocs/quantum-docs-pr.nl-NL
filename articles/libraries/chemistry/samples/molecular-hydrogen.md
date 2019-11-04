---
title: Schattingen voor het energie niveau verkrijgen | Microsoft Docs
description: Documenten met een schatting van het energie niveau verkrijgen
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.energyestimate
ms.openlocfilehash: 0fd457b152083af364d924502c18bc0813e34b83
ms.sourcegitcommit: aa5e6f4a2deb4271a333d3f1b1eb69b5bb9a7bad
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/02/2019
ms.locfileid: "73442572"
---
# <a name="obtaining-energy-level-estimates"></a>Schattingen van energieniveaus maken
Het schatten van de waarden van energie niveaus is een van de belangrijkste toepassingen van quantum chemie. Hier wordt uitgelegd hoe dit kan worden uitgevoerd voor het canonieke voor beeld van moleculaire water stof. Het voor beeld waarnaar in deze sectie wordt verwezen, is `MolecularHydrogen` in de bibliotheek met schei kunde-voor beelden. Een meer visueel voor beeld van het uitzetten van de uitvoer is de `MolecularHydrogenGUI` demo.

Onze eerste stap bestaat uit het samen stellen van de Hamiltonian die moleculaire water stof vertegenwoordigen. Hoewel dit kan worden samengesteld via het NWChem-hulp programma, voegen we hand matig Hamiltonian-voor waarden toe voor het boogere in dit voor beeld.

```csharp
    // These orbital integrals are represented using the OrbitalIntegral
    // data structure.
    var energyOffset = 0.713776188; // This is the coulomb repulsion
    var nElectrons = 2; // Molecular hydrogen has two electrons
    var orbitalIntegrals = new OrbitalIntegral[]
    {
        new OrbitalIntegral(new[] { 0,0 }, -1.252477495),
        new OrbitalIntegral(new[] { 1,1 }, -0.475934275),
        new OrbitalIntegral(new[] { 0,0,0,0 }, 0.674493166),
        new OrbitalIntegral(new[] { 0,1,0,1 }, 0.181287518),
        new OrbitalIntegral(new[] { 0,1,1,0 }, 0.663472101),
        new OrbitalIntegral(new[] { 1,1,1,1 }, 0.697398010),
        // This line adds the identity term.
        new OrbitalIntegral(new int[] { }, energyOffset)
    };

    // We initialize a fermion Hamiltonian data structure and add terms to it.
    var fermionHamiltonian = new OrbitalIntegralHamiltonian(orbitalIntegrals).ToFermionHamiltonian();
```

Voor het simuleren van de Hamiltonian moet ons de fermion-Opera tors converteren naar Qubit-Opera tors. Deze conversie wordt als volgt uitgevoerd via de Wigner-code ring van Jordanië:

```csharp
    // The Jordan-Wigner encoding converts the fermion Hamiltonian, 
    // expressed in terms of fermionic operators, to a qubit Hamiltonian,
    // expressed in terms of Pauli matrices. This is an essential step
    // for simulating our constructed Hamiltonians on a qubit quantum
    // computer.
    var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(Pauli.QubitEncoding.JordanWigner);

    // We also need to create an input quantum state to this Hamiltonian.
    // Let us use the Hartree-Fock state.
    var fermionWavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons);

    // This Jordan-Wigner data structure also contains a representation 
    // of the Hamiltonian and wavefunction made for consumption by the Q# operations.
    var qSharpHamiltonianData = jordanWignerEncoding.ToQSharpFormat();
    var qSharpWavefunctionData = fermionWavefunction.ToQSharpFormat();
    var qSharpData = QSharpFormat.Convert.ToQSharpFormat(qSharpHamiltonianData, qSharpWavefunctionData);
```

Nu worden de `qSharpData` die de Hamiltonian vertegenwoordigt, door gegeven aan de `TrotterStepOracle` functie in [simulatie van Hamiltonian Dynamics](xref:microsoft.quantum.libraries.standard.algorithms). `TrotterStepOracle` retourneert een Quantum bewerking die de real-time-evolutie van de Hamiltonian benadert.

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// Choose the integrator step size
let stepSize = 1.0;

// Choose the order of the Trotter—Suzuki integrator.
let integratorOrder = 4;

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/stepSize` -- the number of steps required to simulate unit-time evolution.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operatrion.
let (nQubits, (rescale, oracle)) =  TrotterStepOracle (qSharpData, stepSize, integratorOrder);
```

We kunnen nu de fase schattings algoritmen van de standaard bibliotheek gebruiken om de bodem status energie te leren gebruiken met behulp van de bovenstaande simulatie. Hiervoor moet een goede benadering van de Quantum status worden voor bereid. Suggesties voor dergelijke benaderingen zijn te vinden in het `Broombridge`-schema, maar deze suggesties worden niet door de standaard benadering toegevoegd, maar er wordt een aantal `hamiltonian.NElectrons` electrons aan greedily geminimaliseerd om het Energies voor de diagonaal één-elektro periode te minimaliseren. De functies en bewerkingen van de fase-schatting bevinden zich in de [naam ruimte micro soft. Quantum. kenmerkt](xref:microsoft.quantum.characterization in DocFX notation).

Het volgende code fragment laat zien hoe de uitvoer van real-time-evolutie door de simulatie bibliotheek voor chemie kan worden geïntegreerd met de Quantum Phase-schatting.

```qsharp
operation GetEnergyByTrotterization (
    qSharpData : JordanWignerEncodingData, 
    nBitsPrecision : Int, 
    trotterStepSize : Double, 
    trotterOrder : Int) : (Double, Double) {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    let (nSpinOrbitals, fermionTermData, statePrepData, energyOffset) = qSharpData!;
    
    // We use a Product formula, also known as `Trotterization` to
    // simulate the Hamiltonian.
    let (nQubits, (rescaleFactor, oracle)) = 
        TrotterStepOracle(qSharpData, trotterStepSize, trotterOrder);
    
    // The operation that creates the trial state is defined below.
    // By default, greedy filling of spin-orbitals is used.
    let statePrep = PrepareTrialState(statePrepData, _);
    
    // We use the Robust Phase Estimation algorithm
    // of Kimmel, Low and Yoder.
    let phaseEstAlgorithm = RobustPhaseEstimation(nBitsPrecision, _, _);
    
    // This runs the quantum algorithm and returns a phase estimate.
    let estPhase = EstimateEnergy(nQubits, statePrep, oracle, phaseEstAlgorithm);
    
    // We obtain the energy estimate by rescaling the phase estimate
    // with the trotterStepSize. We also add the constant energy offset
    // to the estimated energy.
    let estEnergy = estPhase * rescaleFactor + energyOffset;
    
    // We return both the estimated phase, and the estimated energy.
    return (estPhase, estEnergy);
}
```

Deze Q #-code kan nu worden aangeroepen vanuit het stuur programma. In het volgende wordt een volle versie van de simulator gemaakt en wordt `GetEnergyByTrotterization` uitgevoerd om de grond energie te verkrijgen.

```csharp
using (var qsim = new QuantumSimulator())
{
    // We specify the bits of precision desired in the phase estimation 
    // algorithm
    var bits = 7;

    // We specify the step-size of the simulated time-evolution. This needs to
    // be small enough to avoid aliasing of phases, and also to control the
    // error of simulation.
    var trotterStep = 0.4;

    // Choose the Trotter integrator order
    Int64 trotterOrder = 1;

    // As the quantum algorithm is probabilistic, let us run a few trials.

    // This may be compared to true value of
    Console.WriteLine("Exact molecular Hydrogen ground state energy: -1.137260278.\n");
    Console.WriteLine("----- Performing quantum energy estimation by Trotter simulation algorithm");
    for (int i = 0; i < 5; i++)
    {
        // EstimateEnergyByTrotterization
        var (phaseEst, energyEst) = GetEnergyByTrotterization.Run(qsim, qSharpData, bits, trotterStep, trotterOrder).Result;
    }
}
```

Houd er rekening mee dat er twee para meters worden geretourneerd. `energyEst` is de schatting van het energie verbruik van de grond, en moet gemiddeld rond `-1.137` zijn. `phaseEst` is de onbewerkte fase die wordt geretourneerd door het fase schattings algoritme en is nuttig bij het vaststellen van de manier waarop aliassen worden uitgevoerd als gevolg van een `trotterStep` dat te groot is.
