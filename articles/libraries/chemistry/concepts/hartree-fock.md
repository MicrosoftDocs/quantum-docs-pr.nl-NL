---
title: Hartree-Fock theorie
description: Meer informatie over de Hartree – Fock theorie, een eenvoudige manier om de initiële status voor Quantum systemen samen te stellen.
author: nathanwiebe2
ms.author: nawiebe@microsoft.com
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.hartreefock
ms.openlocfilehash: 6fa63cbe13fe98565ffb42b56f3ade86720cedb3
ms.sourcegitcommit: 6ccea4a2006a47569c4e2c2cb37001e132f17476
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "77904448"
---
# <a name="hartreefock-theory"></a>Hartree – Fock theorie

Misschien is de belangrijkste hoeveelheid in de vorm van een gesimuleerde simulatie de grond, het minimale energie eigenvector van de Hamiltonian-matrix.
Dit komt doordat voor de meeste moleculen bij kamer temperatuur aantallen, zoals reactie snelheden, worden gedominerend door de vrije energie verschillen tussen de Quantum staten die het begin en het einde van een stap in een reactie traject beschrijven en bij kamer temperatuur van dergelijke tussenliggende de status is doorgaans de grond.
Hoewel de grond status meestal te moeilijk te leren is (zelfs met een quantum computer), omdat het een distributie is over een exponentieel groot aantal configuraties.
Hoeveel heden, zoals grond energie, kunnen worden geleerd.
Als $ \ket{\psi} $ bijvoorbeeld een zuivere Quantum status is, dan \begin{Equation} E = \bra{\psi} \hat{H} \ket{\psi} \end{Equation} de gemiddelde energie die het systeem in die staat heeft.
De grond staat vervolgens de status die de kleinste waarde geeft. Als gevolg hiervan is het kiezen van een staat die zo dicht mogelijk bij de werkelijke toestand ligt, van cruciaal belang voor het rechtstreeks schatten van de energie (zoals uitgevoerd in variatie eigensolvers) of door de fase schatting.

Hartree – Fock theorie biedt een eenvoudige manier om de initiële status voor Quantum systemen samen te stellen. Het levert een enkele Slater-determinant benadering van de bodem status van een Quantum systeem. In dat geval vindt een rotatie plaats in de Fock-ruimte die het energie verbruik van de grond toestand minimaliseert. Met name voor een systeem van $N $ electrons heeft de methode de draai \begin{Equation} \ prod_ {j = 0} ^ {N-1} a ^ \ dagger_j \ket{0} \mapsto \ prod_ {j = 0} ^ {N-1} e ^ {u} a ^ \ dagger_j e ^ {-u} \ket{0}\defeq\ prod_ {j = 0} ^ {N-1} \widetilde{a} ^ \ dagger_j \ket{0}, \end{Equation} met een anti-Hermitian (dat wil zeggen $u =-u ^ \dagger $) matrix $u = \ sum_ {pq} u_ {pq} a ^ \ dagger_p a_q $. U moet erop gewezen dat de matrix $u $ de Orbital-rotaties en $ \widetilde{a} ^ \ dagger_j $ en $ \widetilde{a} _j $ representeert en Annihilation Opera tors voor electrons die in Hartree worden gehouden.


De matrix $u $ wordt vervolgens geoptimaliseerd om de verwachte energie $ \bra{0} \ prod_ {j = 0} ^ {N-1} \widetilde{a}\_j H \prod\_{k = 0} ^ {N-1} \widetilde{a} ^ \ dagger_k \ket{0}$ te minimaliseren. Hoewel dergelijke optimalisatie problemen algemeen moeilijk zijn, is het Hartree-Fock-algoritme in de praktijk doorgaans snel te convergeren naar een nabije optimale oplossing voor het optimaliserings probleem, met name voor moleculen van gesloten-shells in de evenwichts geometrie. We kunnen deze statussen opgeven als een exemplaar van het `FermionWavefunction`-object. De status $a ^ \ dagger_{1}een ^ \ dagger_{2}een ^ \ dagger_{6}\ket{0}$ wordt als volgt in de Library voor schei kunde geïnstantieerd.
```csharp
// Create a list of integer indices of the creation operators
var indices = new[] { 1, 2, 6 };

// Convert the list of indices to a `FermionWavefunction` object.
// In this case, the indices are integers, so we use the `int`
// type specialization.
var wavefunction = new FermionWavefunction<int>(indices);
```
Het is ook mogelijk om Wave-functies te indexeren met `SpinOrbital` indices en deze indexen vervolgens als volgt te converteren naar gehele getallen.
```csharp
// Create a list of spin orbital indices of the creation operators
var indices = new[] { (0, Spin.d), (1,Spin.u), (3, Spin.u) };

// Convert the list of indices to a `FermionWavefunction` object.
var wavefunctionSpinOrbital = new FermionWavefunction<SpinOrbital>(indices.ToSpinOrbitals());

// Convert a wavefunction indexed by spin orbitals to
// one indexed by integers
var wavefunctionInt = wavefunctionSpinOrbital.ToIndexing(IndexConvention.UpDown);
```

De meest Ophalende functie over Hartree – Fock theorie is dat deze een Quantum status levert die geen entanglement tussen de electrons heeft.
Dit betekent dat het vaak een geschikte kwalitatieve beschrijving van de eigenschappen van moleculaire systemen bevat. 

De Hartree-Fock-status kan ook als volgt worden gereconstrueerd van een `FermionHamiltonian`.
```csharp
// We initialize a fermion Hamiltonian.
var fermionHamiltonian = new FermionHamiltonian();

// Create a Hartree-Fock state from the Hamiltonian 
// with, say, `4` occupied spin orbitals.
var wavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons: 4);
```

Om nauw keurige resultaten te verkrijgen, met name voor sterk gecorreleerde systemen, moet u echter wel Quantum statussen hebben die verder gaan dan Hartree – Fock theorie.
