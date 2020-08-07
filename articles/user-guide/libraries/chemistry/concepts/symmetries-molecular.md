---
title: Symmetries van moleculaire integralen
description: Meer informatie over het gebruik van het Q# OrbitalIntegral-type voor het opsommen van moleculaire Symmetries.
author: nathanwiebe2
ms.author: nawiebe
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.symmetries
no-loc:
- Q#
- $$v
ms.openlocfilehash: 1f71c0ac8e2cd2781c0bc7b23d6c9222f3b9d18a
ms.sourcegitcommit: 6bf99d93590d6aa80490e88f2fd74dbbee8e0371
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/06/2020
ms.locfileid: "87869440"
---
# <a name="symmetries-of-molecular-integrals"></a>Symmetries van moleculaire integralen

De inherente symmetrie van de Coulomb-Hamiltonian, dat wil zeggen de Hamiltonian in [Quantum modellen voor elektronische systemen](xref:microsoft.quantum.chemistry.concepts.quantummodels), waarin electrons interacties met elkaar en de nuclei wordt beschreven, leidt tot een aantal Symmetries dat kan worden misbruikt om de voor waarden in de Hamiltonian te comprimeren.
Over het algemeen als er geen verdere veronderstellingen worden gemaakt over de basis functies $ \ psi_j $, hebben we alleen die \begin{Equation} h_ {pqrs} = h_ {qpsr}, \tag{★} \label{EQ: hpqrs} \end{Equation} die direct kan worden gezien in de integralen in [Quantum modellen voor elektronische systemen](xref:microsoft.quantum.chemistry.concepts.quantummodels) , waarbij de waarden identiek blijven als $p, q $ en $r, s $ worden verwisseld van anti-werk.

Als we ervan uitgaan dat de spin-banen een echte waarde hebben (zoals voor de Orbital bases van Gaussiaans), hebben we er nog verder over dat \begin{Equation} h_ {pqrs} = h_ {qpsr} = h_ {srqp} = h_ {rspq} = h_ {rqps} = h_ {psrq} = h_ {SPQR} = h_ {qrsp} .\tag {★} \label{EQ: hpqrsreal} \end{Equation} heeft deze hypo theses geblokkeerd, maar we kunnen de bovenstaande Symmetries gebruiken om de benodigde gegevens te reduceren voor het opslaan van de matrix elementen van de Hamiltonian met een factor van $8 $; Hoewel het importeren van gegevens op een consistente manier iets moeilijker wordt.
Gelukkig heeft de Hamiltonian simulatie bibliotheek subroutines die kunnen worden gebruikt voor het importeren van integrale bestanden uit [LIQUI $ | \rangle $](https://www.microsoft.com/en-us/research/project/language-integrated-quantum-operations-liqui/) of rechtstreeks vanuit [NWChem](http://www.nwchem-sw.org/index.php/Main_Page).

Moleculaire Orbital-integralen (de $h \_ {pq} $ en $h \_ {pqrs} $ termen) zoals deze worden weer gegeven met behulp `OrbitalIntegral` van het type, dat een aantal handige functies biedt om deze symmetrie uit te drukken.
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

Naast het opsommen van alle Orbital-integralen die numeriek identiek zijn, wordt een lijst met alle Orbital-indexen die zijn opgenomen in de Hamiltonian vertegenwoordigd door een, `OrbitalIntegral` als volgt gegenereerd.
```csharp
    // Create a `OrbitalIntegral` instance to store a two-electron molecular
    // orbital integral data.
    var twoElectronIntegral = new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123);

    // This enumerates all spin-orbital indices of the `FermionTerm`s in the 
    // Hamiltonian represented by this integral -- this is an array of array 
    // of `SpinOrbital` instances.
    var twoElectronSpinOrbitalIndices = twoElectronIntegral.EnumerateSpinOrbitals();
```
## <a name="constructing-fermionic-hamiltonians-from-molecular-integrals"></a>Fermionic Hamiltonians maken op basis van moleculaire integralen

In plaats van een Fermionic-Hamiltonian te maken door een s toe te voegen `FermionTerm` , kunnen alle termen die overeenkomen met elke Orbital-integraal automatisch worden toegevoegd.
De volgende code geeft bijvoorbeeld automatisch een opsomming van alle permutatieve Symmetries en rangschikt de voor waarden in canonieke volg orde: 
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
