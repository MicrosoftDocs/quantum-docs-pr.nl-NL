---
title: Symmetries van moleculaire integralen
description: 'Meer informatie over het gebruik van het type Q # OrbitalIntegral voor het opsommen van moleculaire Symmetries.'
author: nathanwiebe2
ms.author: nawiebe
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.symmetries
ms.openlocfilehash: b7e7b79af17af544c4a784eff08500498afc9f67
ms.sourcegitcommit: 0181e7c9e98f9af30ea32d3cd8e7e5e30257a4dc
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2020
ms.locfileid: "85274474"
---
# <a name="symmetries-of-molecular-integrals"></a><span data-ttu-id="d8b2d-103">Symmetries van moleculaire integralen</span><span class="sxs-lookup"><span data-stu-id="d8b2d-103">Symmetries of Molecular Integrals</span></span>

<span data-ttu-id="d8b2d-104">De inherente symmetrie van de Coulomb-Hamiltonian, dat wil zeggen de Hamiltonian in [Quantum modellen voor elektronische systemen](xref:microsoft.quantum.chemistry.concepts.quantummodels), waarin electrons interacties met elkaar en de nuclei wordt beschreven, leidt tot een aantal Symmetries dat kan worden misbruikt om de voor waarden in de Hamiltonian te comprimeren.</span><span class="sxs-lookup"><span data-stu-id="d8b2d-104">The inherent symmetry of the Coulomb Hamiltonian, which is the Hamiltonian given in [Quantum Models for Electronic Systems](xref:microsoft.quantum.chemistry.concepts.quantummodels), that describes electrons interacting electrically with each other and with the nuclei, leads to a number of symmetries that can be exploited to compress the terms in the Hamiltonian.</span></span>
<span data-ttu-id="d8b2d-105">Over het algemeen als er geen verdere veronderstellingen worden gemaakt over de basis functies $ \ psi_j $, hebben we alleen die \begin{Equation} h_ {pqrs} = h_ {qpsr}, \tag{★} \label{EQ: hpqrs} \end{Equation} die direct kan worden gezien in de integralen in [Quantum modellen voor elektronische systemen](xref:microsoft.quantum.chemistry.concepts.quantummodels) , waarbij de waarden identiek blijven als $p, q $ en $r, s $ worden verwisseld van anti-werk.</span><span class="sxs-lookup"><span data-stu-id="d8b2d-105">In general if no further assumptions are made about the basis functions $\psi_j$ then we only have that \begin{equation} h_{pqrs}= h_{qpsr},\tag{★}\label{eq:hpqrs} \end{equation} which can be immediately seen from the integrals in [Quantum Models for Electronic Systems](xref:microsoft.quantum.chemistry.concepts.quantummodels) upon noting that their values remain identical if $p,q$ and $r,s$ are interchanged from anti-commutation.</span></span>

<span data-ttu-id="d8b2d-106">Als we ervan uitgaan dat de spin-banen een echte waarde hebben (zoals voor de Orbital bases van Gaussiaans), hebben we er nog verder over dat \begin{Equation} h_ {pqrs} = h_ {qpsr} = h_ {srqp} = h_ {rspq} = h_ {rqps} = h_ {psrq} = h_ {SPQR} = h_ {qrsp} .\tag {★} \label{EQ: hpqrsreal} \end{Equation} heeft deze hypo theses geblokkeerd, maar we kunnen de bovenstaande Symmetries gebruiken om de benodigde gegevens te reduceren voor het opslaan van de matrix elementen van de Hamiltonian met een factor van $8 $; Hoewel het importeren van gegevens op een consistente manier iets moeilijker wordt.</span><span class="sxs-lookup"><span data-stu-id="d8b2d-106">If we assume that the spin-orbitals are real-valued (as they are for Gaussian orbital bases) then we further have that \begin{equation} h_{pqrs} = h_{qpsr} = h_{srqp} = h_{rspq}=h_{rqps}=h_{psrq}=h_{spqr}=h_{qrsp}.\tag{★}\label{eq:hpqrsreal} \end{equation} Given such assumptions hold, we can use the above symmetries to reduce the data needed to store the matrix elements of the Hamiltonian by a factor of $8$; although doing so makes importing data in a consistent way slightly more challenging.</span></span>
<span data-ttu-id="d8b2d-107">Gelukkig heeft de Hamiltonian simulatie bibliotheek subroutines die kunnen worden gebruikt voor het importeren van integrale bestanden uit [LIQUI $ | \rangle $](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/) of rechtstreeks vanuit [NWChem](http://www.nwchem-sw.org/index.php/Main_Page).</span><span class="sxs-lookup"><span data-stu-id="d8b2d-107">Fortunately the Hamiltonian simulation library has subroutines that can be used to import integral files from either [LIQUI$|\rangle$](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/) or directly from [NWChem](http://www.nwchem-sw.org/index.php/Main_Page).</span></span>

<span data-ttu-id="d8b2d-108">Moleculaire Orbital-integralen (de $h \_ {pq} $ en $h \_ {pqrs} $ termen) zoals deze worden weer gegeven met behulp `OrbitalIntegral` van het type, dat een aantal handige functies biedt om deze symmetrie uit te drukken.</span><span class="sxs-lookup"><span data-stu-id="d8b2d-108">Molecular orbital integrals (i.e. the $h\_{pq}$ and $h\_{pqrs}$ terms) such as these are represented using the `OrbitalIntegral` type, which provides a number of helpful functions to express this symmetry.</span></span>
```csharp
    // Load the namespace containing orbital integral objects.
    using Microsoft.Quantum.Chemistry.OrbitalIntegrals;

    // Create a `OrbitalIntegral` instance to store a one-electron molecular 
    // orbital integral data.
    var oneElectronOrbitalIndices = new[] { 0, 1 };
    var oneElectronCoefficient = 1.0;
    var oneElectronIntegral = new OrbitalIntegral(oneElectronOrbitalIndices, oneElectronCoefficient);

    // This enumerates all one-electron integrals with the same coefficient --
    // an array of equivalent `OrbitalIntegral` instances is generated. In this
    // case, there are two elements.
    var oneElectronIntegrals = oneElectronIntegral.EnumerateOrbitalSymmetries();

    // Create a `OrbitalIntegral` instance to store a two-electron molecular orbital integral data.
    var twoElectronOrbitalIndices = new[] { 0, 1, 2, 3 };
    var twoElectronCoefficient = 0.123;
    var twoElectronIntegral = new OrbitalIntegral(twoElectronOrbitalIndices, twoElectronCoefficient);

    // This enumerates all two-electron integrals with the same coefficient -- 
    // an array of equivalent `OrbitalIntegral` instances is generated. In 
    // this case, there are 8 elements.
    var twoElectronIntegrals = twoElectronIntegral.EnumerateOrbitalSymmetries();
```

<span data-ttu-id="d8b2d-109">Naast het opsommen van alle Orbital-integralen die numeriek identiek zijn, wordt een lijst met alle Orbital-indexen die zijn opgenomen in de Hamiltonian vertegenwoordigd door een, `OrbitalIntegral` als volgt gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="d8b2d-109">In addition to enumerating over all orbital integrals that are numerically identical, a list of all spin-orbital indices contained in the Hamiltonian represented by an `OrbitalIntegral` may be generated as follows.</span></span>
```csharp
    // Create a `OrbitalIntegral` instance to store a two-electron molecular
    // orbital integral data.
    var twoElectronIntegral = new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123);

    // This enumerates all spin-orbital indices of the `FermionTerm`s in the 
    // Hamiltonian represented by this integral -- this is an array of array 
    // of `SpinOrbital` instances.
    var twoElectronSpinOrbitalIndices = twoElectronIntegral.EnumerateSpinOrbitals();
```
## <a name="constructing-fermionic-hamiltonians-from-molecular-integrals"></a><span data-ttu-id="d8b2d-110">Fermionic Hamiltonians maken op basis van moleculaire integralen</span><span class="sxs-lookup"><span data-stu-id="d8b2d-110">Constructing Fermionic Hamiltonians from Molecular Integrals</span></span>

<span data-ttu-id="d8b2d-111">In plaats van een Fermionic-Hamiltonian te maken door een s toe te voegen `FermionTerm` , kunnen alle termen die overeenkomen met elke Orbital-integraal automatisch worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="d8b2d-111">Rather than constructing a Fermionic Hamiltonian by adding `FermionTerm`s, all terms corresponding to each orbital integral may be added automatically.</span></span>
<span data-ttu-id="d8b2d-112">De volgende code geeft bijvoorbeeld automatisch een opsomming van alle permutatieve Symmetries en rangschikt de voor waarden in canonieke volg orde:</span><span class="sxs-lookup"><span data-stu-id="d8b2d-112">For example, the following code automatically enumerates over all permutational symmetries and orders the terms in canonical order:</span></span> 
```csharp
    // Load the namespace containing fermion objects. This
    // example also uses LINQ queries.
    using Microsoft.Quantum.Chemistry.Fermion;
    using System.Linq;

    // Create a `OrbitalIntegral` instance to store a two-electron molecular 
    // orbital integral data.
    var orbitalIntegral = new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123);

    // Create an `OrbitalIntegralHamiltonian` instance to store the orbital integral
    // terms
    var orbitalIntegralHamiltonian = new OrbitalIntegralHamiltonian();
    orbitalIntegralHamiltonian.Add(orbitalIntegral);

    // Convert the orbital integral representation to a fermion
    // representation. This also requires choosing a convention for 
    // mapping spin orbital indices to integer indices.
    var fermionHamiltonian = orbitalIntegralHamiltonian.ToFermionHamiltonian(IndexConvention.UpDown);

    // Alternatively, one can add orbital integrals directly to a fermion Hamiltonian
    // as follows. This automatically enumerates over all symmetries, and then
    // orders the `HermitianFermionTerm` instances in canonical order. We will need to
    // choose an indexing convention as well.
    fermionHamiltonian.AddRange(orbitalIntegral
        .ToHermitianFermionTerms(0, IndexConvention.UpDown)
        .Select(o => (o.Item1, o.Item2.ToDoubleCoeff())));
```