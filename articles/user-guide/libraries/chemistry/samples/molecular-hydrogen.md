---
title: Schattingen van energieniveaus maken
description: 'Door loop een voor beeld van een Q #-programma dat de waarden voor het energie niveau van moleculaire water stof schat.'
author: guanghaolow
ms.author: gulow
ms.date: 10/23/2018
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.examples.energyestimate
ms.openlocfilehash: 3242d8c6dc6fad2bd99055027dd7ce4ec3510ff4
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85275157"
---
# <a name="obtaining-energy-level-estimates"></a><span data-ttu-id="e7948-103">Schattingen van energieniveaus maken</span><span class="sxs-lookup"><span data-stu-id="e7948-103">Obtaining energy level estimates</span></span>
<span data-ttu-id="e7948-104">Het schatten van de waarden van energie niveaus is een van de belangrijkste toepassingen van quantum chemie.</span><span class="sxs-lookup"><span data-stu-id="e7948-104">Estimating the values of energy levels is one of the principal applications of quantum chemistry.</span></span> <span data-ttu-id="e7948-105">Hier wordt uitgelegd hoe dit kan worden uitgevoerd voor het canonieke voor beeld van moleculaire water stof.</span><span class="sxs-lookup"><span data-stu-id="e7948-105">Here, we outline how this may be performed for the canonical example of molecular Hydrogen.</span></span> <span data-ttu-id="e7948-106">Het voor beeld waarnaar in deze sectie wordt verwezen, bevindt zich `MolecularHydrogen` in de opslag plaats voor schei steek proeven.</span><span class="sxs-lookup"><span data-stu-id="e7948-106">The sample referenced in this section is `MolecularHydrogen` in the chemistry samples repository.</span></span> <span data-ttu-id="e7948-107">Een meer visueel voor beeld van het uitzetten van de uitvoer is de `MolecularHydrogenGUI` demo.</span><span class="sxs-lookup"><span data-stu-id="e7948-107">A more visual example that plots the output is the `MolecularHydrogenGUI` demo.</span></span>

<span data-ttu-id="e7948-108">Onze eerste stap bestaat uit het samen stellen van de Hamiltonian die moleculaire water stof vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="e7948-108">Our first step is to construct the Hamiltonian representing molecular Hydrogen.</span></span> <span data-ttu-id="e7948-109">Hoewel dit kan worden samengesteld via het NWChem-hulp programma, voegen we hand matig Hamiltonian-voor waarden toe voor het boogere in dit voor beeld.</span><span class="sxs-lookup"><span data-stu-id="e7948-109">Though this can be constructed through the NWChem tool, we manually add Hamiltonian terms for brevity in this sample.</span></span>

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

<span data-ttu-id="e7948-110">Voor het simuleren van de Hamiltonian moet ons de fermion-Opera tors converteren naar Qubit-Opera tors.</span><span class="sxs-lookup"><span data-stu-id="e7948-110">Simulating the Hamiltonian requires us to convert the fermion operators to qubit operators.</span></span> <span data-ttu-id="e7948-111">Deze conversie wordt als volgt uitgevoerd via de Wigner-code ring van Jordanië:</span><span class="sxs-lookup"><span data-stu-id="e7948-111">This conversion is performed through the Jordan-Wigner encoding as follows.</span></span>

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

<span data-ttu-id="e7948-112">We geven nu de `qSharpData` Hamiltonian door aan de `TrotterStepOracle` functie in [simulatie van Hamiltonian Dynamics](xref:microsoft.quantum.libraries.standard.algorithms).</span><span class="sxs-lookup"><span data-stu-id="e7948-112">We now pass the `qSharpData` representing the Hamiltonian to the `TrotterStepOracle` function in [Simulating Hamiltonian dynamics](xref:microsoft.quantum.libraries.standard.algorithms).</span></span> <span data-ttu-id="e7948-113">`TrotterStepOracle`retourneert een Quantum bewerking die de real-time-evolutie van de Hamiltonian benadert.</span><span class="sxs-lookup"><span data-stu-id="e7948-113">`TrotterStepOracle` returns a quantum operation that approximates the real time-evolution of the Hamiltonian.</span></span>

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

<span data-ttu-id="e7948-114">We kunnen nu de fase schattings algoritmen van de standaard bibliotheek gebruiken om de bodem status energie te leren gebruiken met behulp van de bovenstaande simulatie.</span><span class="sxs-lookup"><span data-stu-id="e7948-114">We can now use the standard library's phase estimation algorithms to learn the ground state energy using the above simulation.</span></span> <span data-ttu-id="e7948-115">Hiervoor moet een goede benadering van de Quantum status worden voor bereid.</span><span class="sxs-lookup"><span data-stu-id="e7948-115">This requires preparing a good approximation to the quantum ground state.</span></span> <span data-ttu-id="e7948-116">Suggesties voor dergelijke benaderingen zijn opgenomen in het `Broombridge` schema, maar deze suggesties zijn niet aanwezig. de standaard benadering voegt een aantal `hamiltonian.NElectrons` electrons toe aan greedily om de Energies van de diagonaal één of minder tijd te minimaliseren.</span><span class="sxs-lookup"><span data-stu-id="e7948-116">Suggestions for such approximations are provided in the `Broombridge` schema, but absent these suggestions, the default approach adds a number of `hamiltonian.NElectrons` electrons to  greedily minimize the diagonal one-electron term energies.</span></span> <span data-ttu-id="e7948-117">De functies en bewerkingen van de fase-schatting bevinden zich in de [naam ruimte micro soft. Quantum. kenmerkt](xref:microsoft.quantum.characterization in DocFX notation).</span><span class="sxs-lookup"><span data-stu-id="e7948-117">The phase estimation functions and operations are located in the [Microsoft.Quantum.Characterization namespace](xref:microsoft.quantum.characterization in DocFX notation).</span></span>

<span data-ttu-id="e7948-118">Het volgende code fragment laat zien hoe de uitvoer van real-time-evolutie door de simulatie bibliotheek voor chemie kan worden geïntegreerd met de Quantum Phase-schatting.</span><span class="sxs-lookup"><span data-stu-id="e7948-118">The following snippet shows how the real time-evolution output by the chemistry simulation library may be integrated with quantum phase estimation.</span></span>

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

<span data-ttu-id="e7948-119">Deze Q #-code kan nu worden aangeroepen vanuit het stuur programma.</span><span class="sxs-lookup"><span data-stu-id="e7948-119">This Q# code may now be invoke from the driver program.</span></span> <span data-ttu-id="e7948-120">In het volgende wordt een volledige versie van de simulator gemaakt en uitgevoerd `GetEnergyByTrotterization` om de grond energie te verkrijgen.</span><span class="sxs-lookup"><span data-stu-id="e7948-120">In the following, we create a full-state simulator and run `GetEnergyByTrotterization` to obtain the ground state energy.</span></span>

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

<span data-ttu-id="e7948-121">Houd er rekening mee dat er twee para meters worden geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="e7948-121">Note that two parameters are returned.</span></span> <span data-ttu-id="e7948-122">`energyEst`is de schatting van de grond energie, en moet `-1.137` op gemiddeld worden gesteld.</span><span class="sxs-lookup"><span data-stu-id="e7948-122">`energyEst` is the estimate of the ground state energy, and should be around `-1.137` on average.</span></span> <span data-ttu-id="e7948-123">`phaseEst`is de onbewerkte fase die wordt geretourneerd door het fase schattings algoritme en is nuttig bij het vaststellen van de manier waarop aliassen ontstaan als gevolg van een `trotterStep` te groot.</span><span class="sxs-lookup"><span data-stu-id="e7948-123">`phaseEst` is the raw phase returned by the phase estimation algorithm, and is useful to diagnose when aliasing occurs due to a `trotterStep` that is too large.</span></span>