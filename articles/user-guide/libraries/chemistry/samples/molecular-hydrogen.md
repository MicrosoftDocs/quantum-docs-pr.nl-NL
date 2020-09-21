---
title: Schattingen van energieniveaus maken
description: Een voor beeld Q# van een programma voor het schatten van de waarden van het energie niveau van moleculaire water stof.
author: guanghaolow
ms.author: gulow
ms.date: 07/02/2020
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.energyestimate
no-loc:
- Q#
- $$v
ms.openlocfilehash: 05506f4099de754cd02d81fbd9200f2de091e37e
ms.sourcegitcommit: 8256ff463eb9319f1933820a36c0838cf1e024e8
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/17/2020
ms.locfileid: "90759729"
---
# <a name="obtaining-energy-level-estimates"></a>Schattingen van energieniveaus maken
Het schatten van de waarden van energie niveaus is een van de belangrijkste toepassingen van quantum chemie. In dit artikel wordt beschreven hoe u dit kunt doen voor het canonieke voor beeld van moleculaire water stof. Het voor beeld waarnaar in deze sectie wordt verwezen, bevindt zich [`MolecularHydrogen`](https://github.com/microsoft/Quantum/tree/main/samples/chemistry/MolecularHydrogen) in de opslag plaats voor schei steek proeven. Een meer visueel voor beeld van het uitzetten van de uitvoer is de [`MolecularHydrogenGUI`](https://github.com/microsoft/Quantum/tree/main/samples/chemistry/MolecularHydrogenGUI) demo.

## <a name="estimating-the-energy-values-of-molecular-hydrogen"></a>Schatting van de energie waarden van moleculaire water stof

De eerste stap bestaat uit het samen stellen van de Hamiltonian die moleculaire water stof vertegenwoordigen. Hoewel u dit kunt maken met behulp van het NWChem-hulp programma, worden met dit voor beeld de Hamiltonian-termen hand matig toegevoegd.

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

    // Initialize a fermion Hamiltonian data structure and add terms to it.
    var fermionHamiltonian = new OrbitalIntegralHamiltonian(orbitalIntegrals).ToFermionHamiltonian();
```

Voor het simuleren van de Hamiltonian moet u de fermion-Opera tors converteren naar Qubit-Opera tors. Deze conversie wordt als volgt uitgevoerd via de Wigner-code ring van Jordanië:

```csharp
    // The Jordan-Wigner encoding converts the fermion Hamiltonian, 
    // expressed in terms of fermionic operators, to a qubit Hamiltonian,
    // expressed in terms of Pauli matrices. This is an essential step
    // for simulating our constructed Hamiltonians on a qubit quantum
    // computer.
    var jordanWignerEncoding = fermionHamiltonian.ToPauliHamiltonian(Pauli.QubitEncoding.JordanWigner);

    // You also need to create an input quantum state to this Hamiltonian.
    // Use the Hartree-Fock state.
    var fermionWavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons);

    // This Jordan-Wigner data structure also contains a representation 
    // of the Hamiltonian and wavefunction made for consumption by the Q# operations.
    var qSharpHamiltonianData = jordanWignerEncoding.ToQSharpFormat();
    var qSharpWavefunctionData = fermionWavefunction.ToQSharpFormat();
    var qSharpData = QSharpFormat.Convert.ToQSharpFormat(qSharpHamiltonianData, qSharpWavefunctionData);
```

Geef vervolgens door `qSharpData` dat de Hamiltonian wordt aangeduid met de `TrotterStepOracle` functie. `TrotterStepOracle` retourneert een Quantum bewerking die de realtime-evolutie van de Hamiltonian benadert. Zie [Hamiltonian Dynamics simuleren](xref:microsoft.quantum.chemistry.concepts.simulationalgorithms)voor meer informatie.

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// Choose the integrator step size
let stepSize = 1.0;

// Choose the order of the Trotter—Suzuki integrator.
let integratorOrder = 4;

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/stepSize` -- the number of steps required to simulate unit-time evolution.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operation.
let (nQubits, (rescale, oracle)) =  TrotterStepOracle (qSharpData, stepSize, integratorOrder);
```

Op dit moment kunt u de [fase schattings algoritmen](xref:microsoft.quantum.libraries.characterization) van de standaard bibliotheek gebruiken om de status van de grond energie te lezen met behulp van de vorige simulatie. Hiervoor moet een goede benadering van de Quantum status worden voor bereid. Suggesties voor dergelijke benaderingen zijn opgenomen in het [`Broombridge`](xref:microsoft.quantum.libraries.chemistry.schema.broombridge) schema. Als deze suggesties echter niet aanwezig zijn, voegt de standaard benadering een aantal `hamiltonian.NElectrons` electrons toe aan greedily om de diagonale termijn van één of meer Energies te minimaliseren. De fase schattings functies en-bewerkingen zijn te vinden in de DocFX-notatie in de [micro soft. Quantum. kenmerkt](xref:microsoft.quantum.characterization) -naam ruimte.

Het volgende code fragment laat zien hoe de real-time ontwikkelings uitvoer van de werk bibliotheek voor schei kunde kan worden geïntegreerd met de Quantum-fase schatting.

```qsharp
operation GetEnergyByTrotterization (
    qSharpData : JordanWignerEncodingData, 
    nBitsPrecision : Int, 
    trotterStepSize : Double, 
    trotterOrder : Int) : (Double, Double) {
    
    // The data describing the Hamiltonian for all these steps is contained in
    // `qSharpData`
    let (nSpinOrbitals, fermionTermData, statePrepData, energyOffset) = qSharpData!;
    
    // Using a Product formula, also known as `Trotterization`, to
    // simulate the Hamiltonian.
    let (nQubits, (rescaleFactor, oracle)) = 
        TrotterStepOracle(qSharpData, trotterStepSize, trotterOrder);
    
    // The operation that creates the trial state is defined here.
    // By default, greedy filling of spin-orbitals is used.
    let statePrep = PrepareTrialState(statePrepData, _);
    
    // Using the Robust Phase Estimation algorithm
    // of Kimmel, Low and Yoder.
    let phaseEstAlgorithm = RobustPhaseEstimation(nBitsPrecision, _, _);
    
    // This runs the quantum algorithm and returns a phase estimate.
    let estPhase = EstimateEnergy(nQubits, statePrep, oracle, phaseEstAlgorithm);
    
    // Now, obtain the energy estimate by rescaling the phase estimate
    // with the trotterStepSize. We also add the constant energy offset
    // to the estimated energy.
    let estEnergy = estPhase * rescaleFactor + energyOffset;
    
    // Return both the estimated phase and the estimated energy.
    return (estPhase, estEnergy);
}
```

U kunt de code nu oproepen Q# vanuit het hostprogramma. Met de volgende C#-code wordt een volledige status Simulator gemaakt en wordt uitgevoerd `GetEnergyByTrotterization` om de grond energie te verkrijgen.

```csharp
using (var qsim = new QuantumSimulator())
{
    // Specify the bits of precision desired in the phase estimation 
    // algorithm
    var bits = 7;

    // Specify the step size of the simulated time evolution. The step size needs to
    // be small enough to avoid aliasing of phases, and also to control the
    // error of simulation.
    var trotterStep = 0.4;

    // Choose the Trotter integrator order
    Int64 trotterOrder = 1;

    // As the quantum algorithm is probabilistic, run a few trials.

    // This may be compared to true value of
    Console.WriteLine("Exact molecular hydrogen ground state energy: -1.137260278.\n");
    Console.WriteLine("----- Performing quantum energy estimation by Trotter simulation algorithm");
    for (int i = 0; i < 5; i++)
    {
        // EstimateEnergyByTrotterization
        var (phaseEst, energyEst) = GetEnergyByTrotterization.Run(qsim, qSharpData, bits, trotterStep, trotterOrder).Result;
    }
}
```

De bewerking retourneert twee para meters: 

- `energyEst` is de schatting van de grond energie en moet dicht bij het `-1.137` gemiddelde liggen. 
- `phaseEst` is de onbewerkte fase die wordt geretourneerd door de fase schattings algoritme. Dit is handig voor het oplossen van aliassen wanneer deze zich voordoen als gevolg van een `trotterStep` te grote waarde.
