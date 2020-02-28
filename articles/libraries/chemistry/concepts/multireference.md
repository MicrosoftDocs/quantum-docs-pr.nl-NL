---
title: Gecorreleerde golffuncties
description: Meer informatie over dynamische en niet-dynamische correlaties in wavefunctions met behulp van de micro soft quantum chemie-bibliotheek.
author: guanghaolow
ms.author: gulow@microsoft.com
ms.date: 05/28/2019
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.multireference
ms.openlocfilehash: 005ef86382ca72969b06a4206cab01f3845718e2
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904431"
---
# <a name="correlated-wavefunctions"></a>Gecorreleerde golffuncties

Voor veel systemen, met name die in de buurt van de evenwichts geometrie, biedt [Hartree – Fock](xref:microsoft.quantum.chemistry.concepts.hartreefock) theorie een kwalitatieve beschrijving van de moleculaire eigenschappen via een verwijzings status met één determinant. Om een kwantitatieve nauw keurigheid te bereiken, moet u echter ook correlatie-effecten overwegen. 

In deze context is het belang rijk om te dinstinguishen tussen dynamische en niet-dynamische correlaties.
Dynamische correlaties ontstaan ten opzichte van de tendens van electrons om elkaar te blijven, zoals bij interelektronische repulsie. Dit effect kan worden gemodelleerd door de electrons uit de referentie status te overwegen. Niet-dynamische correlaties ontstaan wanneer de Wavefunction wordt gecentraliseerd door twee of meer configuraties op zeroth order, zelfs om alleen een kwalitatieve beschrijving van het systeem te krijgen.
Dit vereist een superpositie van determinanten en is een voor beeld van een Wavefunction voor meer informatie.

De Library chemie biedt een manier om een zeroth-Wavefunction op te geven voor het probleem met meer verwijzingen als een superpositie van determinanten. Deze methode, waarmee we sparse Multireference wavefunctions aanroepen, is effectief wanneer slechts enkele onderdelen voldoende zijn om de superpositie op te geven. De bibliotheek biedt ook een methode voor het toevoegen van dynamische correlaties boven op een verwijzing naar één determinant via de gegeneraliseerde unitary gekoppelde-cluster Ansatz. Daarnaast bouwt het ook Quantum circuits die deze statussen op een quantum computer genereren. Deze statussen kunnen worden opgegeven in het [Broombridge-schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)en we bieden ook de functionaliteit om deze statussen hand matig op te geven via de Library chemie.

## <a name="sparse-multi-reference-wavefunction"></a>Sparse multi-Reference Wavefunction
Een status met meerdere verwijzingen $ \ket{\ psi_ {\rm {MCSCF}}} $ kan expliciet worden opgegeven als een lineaire combi natie van $N $-elektroon Slater determininants.
\begin{align} \ket{\ psi_ {\rm {MCSCF}}} \propto \ sum_ {i_1 < i_2 < \cdots < i_N} \ lambda_ {i_1, i_2, \cdots, i_N} a ^ \ dagger_ {i_1} a ^ \ dagger_ {i_2} \cdots a ^ \ dagger_ {i_N} \ket{0}.
\end{align} bijvoorbeeld de status $ \propto (0.1 a ^ \ dagger_1a ^ \ dagger_2a ^ \ dagger_6-0,2 a ^ \ dagger_2a ^ \ dagger_1a ^ \ dagger_5) \ket{0}$ kan als volgt worden opgegeven in de Library chemie.
```csharp
// Create a list of tuples where the first item of each 
// tuple are indices to the creation operators acting on the
// vacuum state, and the second item is the coefficient
// of that basis state.
var superposition = new[] {
    (new[] {1, 2, 6}, 0.1),
    (new[] {2, 1, 5}, -0.2) };

// Create a fermion wavefunction object that represents the superposition.
var wavefunction = new FermionWavefunction<int>(superposition);
```
Deze expliciete weer gave van de superpositie onderdelen is effectief wanneer er slechts enkele onderdelen moeten worden opgegeven. Een voor beeld hiervan is het gebruik van deze representatie als er veel onderdelen nodig zijn om de gewenste status nauw keurig vast te leggen. De reden hiervoor is de degelijkings kosten van het Quantum circuit waarmee deze status wordt voor bereid op een quantum computer, waarmee ten minste lineair wordt geschaald met het aantal superpositie onderdelen, en Maxi maal quadratically met de één norm van de amplitudes van de Super positie.

## <a name="unitary-coupled-cluster-wavefunction"></a>Unitary gekoppeld-cluster Wavefunction
Het is ook mogelijk om een unitary gekoppelde-cluster Wavefunction $ \ket{\ psi_ {\rm {UCC}}} $ op te geven met behulp van de chemistery-bibliotheek. In dit geval hebben we een verwijzings status met één determinant, zegt $ \ket{\ psi_ {\rm{SCF}}} $. De onderdelen van de unitary gekoppelde cluster Wavefunction worden vervolgens impliciet opgegeven via een unitary-operator die wordt uitgevoerd op een referentie status.
Deze unitary-operator wordt meestal geschreven als $e ^ {T-T ^ \dagger} $, waarbij $T-T ^ \dagger $ de anti-Hermitian-cluster operator is. Daarom \begin{align} \ket{\ psi_ {\rm {UCC}}} = e ^ {T-T ^ \dagger}\ket{\ psi_ {\rm{SCF}}}.
\end{align}

Het is ook gebruikelijk om de cluster operator $T = T_1 + T_2 + \cdots $ te splitsen in delen, waarbij elk deel $T _j $ $j $-Body-termen bevat. In gegeneraliseerde gekoppelde cluster theorie is de cluster operator met één hoofd tekst (singles) van het formulier \begin{align} T_1 = \ sum_ {pq} T ^ {p} _ {q} a ^ \ dagger_p a_q, \end{align}

de cluster operator met twee hoofd tekst (dubbels) is van het formulier \begin{align} T_2 = \ sum_ {pqrs} T ^ {pq} _ {RS} a ^ \ dagger_p een ^ \ dagger_q a_r a_s.
\end{align}

De voor waarden voor een hogere volg orde (drieën, 4, enzovoort) zijn mogelijk, maar worden momenteel niet ondersteund door de Library chemie.

Laat bijvoorbeeld $ \ket{\ psi_ {\rm{SCF}}} = a ^ \ dagger_1 een ^ \ dagger_2 \ket{0}$, en laat $T = 0,123 a ^ \ dagger_0 a_1 + 0,456 a ^ \ dagger_0a ^ \ dagger_3 a_1 a_2-0,789 a ^ \ dagger_3a ^ \ dagger_2 a_1 a_0 $. Vervolgens wordt deze status als volgt in de Library chemie geïnstantieerd.
```csharp
// Create a list of indices of the creation operators
// for the single-reference state
var reference = new[] { 1, 2 };

// Create a list describing the cluster operator
// The first half of each list of integers will be
// associated with the creation operators, and
// the second half with the annihilation operators.
var clusterOperator = new[]
{
    (new [] {0, 1}, 0.123),
    (new [] {0, 3, 1, 2}, 0.456),
    (new [] {3, 2, 1, 0}, 0.789)
};

// Create a fermion wavefunction object that represents the 
// unitary coupled-cluster wavefunction. It is assumed implicity
// that the exponent of the unitary coupled-cluster operator
// is the cluster operator minus its Hermitian conjugate.
var wavefunction = new FermionWavefunction<int>(reference, clusterOperator);
```

Kring convervation kunnen expliciet worden gemaakt door `SpinOrbital` indices op te geven in plaats van een geheel getal. Laat bijvoorbeeld $ \ket{\ psi_ {\rm{SCF}}} = a ^ \ dagger_ {1, \uparrow} a ^ \ dagger_ {2, \downarrow}\ket{0}$, en laat $T = 0,123 a ^ \ dagger_ {0, \uparrow} a_ {1, \uparrow} + 0,456 a ^ \ dagger_ {0, \uparrow} a ^ \ dagger_ {3, \downarrow} a_ {1, \uparrow} a_ {2, \downarrow}-0,789 a ^ \ dagger_ {3, \uparrow} a ^ \ dagger_ {2, \uparrow} a_ {1, \uparrow} a_ {0, \uparrow} $ convserving. Vervolgens wordt deze status als volgt in de Library chemie geïnstantieerd.
```csharp
// Create a list of indices of the creation operators
// for the single-reference state
var reference = new[] { (1, Spin.u), (2, Spin.d) }.ToSpinOrbitals();

// Create a list describing the cluster operator
// The first half of each list of integers will be
// associated with the creation operators, and
// the second half with the annihilation operators.
var clusterOperator = new[]
{
    (new [] {(0, Spin.u), (1, Spin.u)}, 0.123),
    (new [] {(0, Spin.u), (3, Spin.d), (1, Spin.u), (2, Spin.d)}, 0.456),
    (new [] {(3, Spin.u), (2, Spin.u), (1, Spin.u), (0, Spin.u)}, 0.789)
}.Select(o => (o.Item1.ToSpinOrbitals(), o.Item2);

// Create a fermion wavefunction object that represents the 
// unitary coupled-cluster wavefunction. It is assumed implicity
// that the exponent of the unitary coupled-cluster operator
// is the cluster operator minus its Hermitian conjugate.
var wavefunctionSpinOrbital = new FermionWavefunction<SpinOrbital>(reference, clusterOperator);

// Convert the wavefunction indexed by spin-orbitals to one indexed
// by integers
var wavefunctionInteger = wavefunctionSpinOrbital.ToIndexing(IndexConvention.UpDown);
```

We bieden ook een gebruiks vriendelijke functie die wordt gebruikt voor het opsommen van alle cluster operators met spin-conversaties die alleen geannihilatede spin-banen hebben en worden gehinderd op alleen onbezette spin-banen.
```csharp
// Create a list of indices of the creation operators
// for the single-reference state
var reference = new[] { (1, Spin.u), (2, Spin.d) }.ToSpinOrbitals();

// Generate all spin-conversing excitations from spin-orbitals 
// occupied by the reference state to virtual orbitals.
var generatedExcitations = reference.CreateAllUCCSDSingletExcitations(nOrbitals: 3).Excitations;

// This is the list of expected spin-consvering excitations
var expectedExcitations = new[]
{
    new []{ (0, Spin.u), (1,Spin.u)},
    new []{ (2, Spin.u), (1,Spin.u)},
    new []{ (0, Spin.d), (2,Spin.d)},
    new []{ (1, Spin.d), (2,Spin.d)},
    new []{ (0, Spin.u), (0, Spin.d), (2, Spin.d), (1,Spin.u)},
    new []{ (0, Spin.u), (1, Spin.d), (2, Spin.d), (1,Spin.u)},
    new []{ (0, Spin.d), (2, Spin.u), (2, Spin.d), (1,Spin.u)},
    new []{ (1, Spin.d), (2, Spin.u), (2, Spin.d), (1,Spin.u)}
}.Select(o => new IndexOrderedSequence<SpinOrbital>(o.ToLadderSequence()));

// The following two assertions are true, and verify that the generated 
// excitations exactly match the expected excitations.
var bool0 = generatedExcitations.Keys.All(expectedExcitations.Contains);
var bool1 = generatedExcitations.Count() == expectedExcitations.Count();
```
