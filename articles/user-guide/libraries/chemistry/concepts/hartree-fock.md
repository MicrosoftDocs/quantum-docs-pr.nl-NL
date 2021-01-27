---
title: Hartree-Fock theorie
description: Meer informatie over de Hartree – Fock theorie, een eenvoudige manier om de initiële status voor Quantum systemen samen te stellen.
author: bradben
ms.author: v-benbra
ms.date: 10/09/2017
ms.topic: conceptual
uid: microsoft.quantum.chemistry.concepts.hartreefock
no-loc:
- Q#
- $$v
ms.openlocfilehash: 48d6bc4face90046271dd8705188a92daafad98a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854096"
---
# <a name="hartreefock-theory"></a><span data-ttu-id="d6381-103">Hartree – Fock theorie</span><span class="sxs-lookup"><span data-stu-id="d6381-103">Hartree–Fock Theory</span></span>

<span data-ttu-id="d6381-104">Misschien is de belangrijkste hoeveelheid in de vorm van een gesimuleerde simulatie de grond, het minimale energie eigenvector van de Hamiltonian-matrix.</span><span class="sxs-lookup"><span data-stu-id="d6381-104">Perhaps the most important quantity in quantum chemistry simulation is the ground state, which is the minimum energy eigenvector of the Hamiltonian matrix.</span></span>
<span data-ttu-id="d6381-105">Dit komt doordat voor de meeste moleculen bij kamer temperatuur aantallen, zoals reactie snelheden, worden gedominerend door de beschik bare energie verschillen tussen de Quantum staten die het begin en het einde van een stap in een reactie traject beschrijven en bij kamer temperatuur, een dergelijke tussenliggende toestand.</span><span class="sxs-lookup"><span data-stu-id="d6381-105">This is because for most molecules at room temperature quantities such as reaction rates are dominated by free energy differences between quantum states that describe the beginning and end of a step in a reaction pathway and at room temperature such intermediate state are usually ground states.</span></span>
<span data-ttu-id="d6381-106">Hoewel de grond status meestal te moeilijk te leren is (zelfs met een quantum computer), omdat het een distributie is over een exponentieel groot aantal configuraties.</span><span class="sxs-lookup"><span data-stu-id="d6381-106">While the ground state is typically too hard to learn (even with a quantum computer) because it is a distribution over an exponentially large number of configurations.</span></span>
<span data-ttu-id="d6381-107">Hoeveel heden, zoals grond energie, kunnen worden geleerd.</span><span class="sxs-lookup"><span data-stu-id="d6381-107">Quantities such as ground state energy can be learned.</span></span>
<span data-ttu-id="d6381-108">Als $ \ket{\psi} $ bijvoorbeeld een zuivere Quantum status is, dan \begin{Equation} E = \bra{\psi} \hat{H} \ket{\psi} \end{Equation} de gemiddelde energie die het systeem in die staat heeft.</span><span class="sxs-lookup"><span data-stu-id="d6381-108">For example, if $\ket{\psi}$ is any pure quantum state then \begin{equation} E = \bra{ \psi } \hat{H} \ket{\psi} \end{equation} gives the mean energy that the system has in that state.</span></span>
<span data-ttu-id="d6381-109">De grond staat vervolgens de status die de kleinste waarde geeft.</span><span class="sxs-lookup"><span data-stu-id="d6381-109">The ground state then is the state that gives the smallest such value.</span></span> <span data-ttu-id="d6381-110">Als gevolg hiervan is het kiezen van een staat die zo dicht mogelijk bij de werkelijke toestand ligt, van cruciaal belang voor het rechtstreeks schatten van de energie (zoals uitgevoerd in variatie eigensolvers) of door de fase schatting.</span><span class="sxs-lookup"><span data-stu-id="d6381-110">As a result, choosing a state that is as close as possible to the true ground state is vitally important for estimating the energy either directly (as is done in variational eigensolvers) or through phase estimation.</span></span>

<span data-ttu-id="d6381-111">Hartree – Fock theorie biedt een eenvoudige manier om de initiële status voor Quantum systemen samen te stellen.</span><span class="sxs-lookup"><span data-stu-id="d6381-111">Hartree–Fock theory gives a simple way to construct the initial state for quantum systems.</span></span> <span data-ttu-id="d6381-112">Het levert een enkele Slater-determinant benadering van de bodem status van een Quantum systeem.</span><span class="sxs-lookup"><span data-stu-id="d6381-112">It yields a single Slater-determinant approximation to the ground state of a quantum system.</span></span> <span data-ttu-id="d6381-113">In dat geval vindt een rotatie plaats in de Fock-ruimte die het energie verbruik van de grond toestand minimaliseert.</span><span class="sxs-lookup"><span data-stu-id="d6381-113">To that end, it finds a rotation within Fock-space that minimizes the ground state energy.</span></span> <span data-ttu-id="d6381-114">Met name voor een systeem van $N $ electrons de methode de draaiing \begin{Equation} \ prod_ {j = 0} ^ {N-1} a ^ \ dagger_j \ket {0} \mapsto \ prod_ {j = 0} ^ {n-1} e ^ {u} a ^ \ dagger_j e ^ {-u} \ket {0} \defeq\ prod_ {j = 0} ^ {N-1} \widetilde{a} ^ \ dagger_j \ket {0} , \end{Equation} met een anti-Hermitian (dat wil zeggen $u =-u ^ \dagger $) matrix $u = \ sum_ {pq} u_ {pq} a ^ \ dagger_p a_q $.</span><span class="sxs-lookup"><span data-stu-id="d6381-114">In particular, for a system of $N$ electrons the method performs the rotation \begin{equation} \prod_{j=0}^{N-1} a^\dagger_j \ket{0} \mapsto \prod_{j=0}^{N-1} e^{u} a^\dagger_j e^{-u} \ket{0}\defeq\prod_{j=0}^{N-1}  \widetilde{a}^\dagger_j  \ket{0}, \end{equation} with an anti-Hermitian (i.e. $u= -u^\dagger$) matrix $u = \sum_{pq} u_{pq} a^\dagger_p a_q$.</span></span> <span data-ttu-id="d6381-115">U moet erop gewezen dat de matrix $u $ de Orbital-rotaties en $ \widetilde{a} ^ \ dagger_j $ en $ \widetilde{a} _j $ representeert en Annihilation Opera tors voor electrons die in Hartree worden gehouden.</span><span class="sxs-lookup"><span data-stu-id="d6381-115">It should be noted that the matrix $u$ represents the orbital rotations and $\widetilde{a}^\dagger_j$ and $\widetilde{a}_j$ represent creation and annihilation operators for electrons occupying Hartree–Fock molecular spin-orbitals.</span></span>


<span data-ttu-id="d6381-116">De matrix $u $ wordt vervolgens geoptimaliseerd om de verwachte energie $ \bra {0} \ prod_ {j = 0} ^ {N-1} \widetilde{a} \_ j H \prod \_ {k = 0} ^ {N-1} \widetilde{a} ^ \ dagger_k \ket $ {0} te minimaliseren.</span><span class="sxs-lookup"><span data-stu-id="d6381-116">The matrix $u$ is then optimized to minimize the expected energy $\bra{0} \prod_{j=0}^{N-1}  \widetilde{a}\_j  H \prod\_{k=0}^{N-1}  \widetilde{a}^\dagger_k\ket{0}$.</span></span> <span data-ttu-id="d6381-117">Hoewel dergelijke optimalisatie problemen algemeen moeilijk zijn, is het Hartree-Fock-algoritme in de praktijk doorgaans snel te convergeren naar een nabije optimale oplossing voor het optimaliserings probleem, met name voor moleculen van gesloten-shells in de evenwichts geometrie.</span><span class="sxs-lookup"><span data-stu-id="d6381-117">While such optimization problems may be generically hard, in practice the Hartree–Fock algorithm tends to rapidly converge to a near-optimal solution to the optimization problem, especially for closed-shell molecules in the equilibrium geometries.</span></span> <span data-ttu-id="d6381-118">We kunnen deze statussen opgeven als een exemplaar van het `FermionWavefunction` object.</span><span class="sxs-lookup"><span data-stu-id="d6381-118">We may specify these states as an instance of the `FermionWavefunction` object.</span></span> <span data-ttu-id="d6381-119">De status $a ^ \ dagger_ {1} een ^ \ dagger_ {2} een ^ \ dagger_ {6} \ket {0} $ wordt als volgt geïnstantieerd in de Library chemie.</span><span class="sxs-lookup"><span data-stu-id="d6381-119">For instance, the state $a^\dagger_{1}a^\dagger_{2}a^\dagger_{6}\ket{0}$ is instantiated in the chemistry library as follows.</span></span>
```csharp
// Create a list of integer indices of the creation operators
var indices = new[] { 1, 2, 6 };

// Convert the list of indices to a `FermionWavefunction` object.
// In this case, the indices are integers, so we use the `int`
// type specialization.
var wavefunction = new FermionWavefunction<int>(indices);
```
<span data-ttu-id="d6381-120">Het is ook mogelijk om Wave-functies te indexeren met `SpinOrbital` indices en deze indexen vervolgens als volgt te converteren naar gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="d6381-120">It is also possible to index wave functions with `SpinOrbital` indices, and then convert these indices to integers as follows.</span></span>
```csharp
// Create a list of spin orbital indices of the creation operators
var indices = new[] { (0, Spin.d), (1,Spin.u), (3, Spin.u) };

// Convert the list of indices to a `FermionWavefunction` object.
var wavefunctionSpinOrbital = new FermionWavefunction<SpinOrbital>(indices.ToSpinOrbitals());

// Convert a wavefunction indexed by spin orbitals to
// one indexed by integers
var wavefunctionInt = wavefunctionSpinOrbital.ToIndexing(IndexConvention.UpDown);
```

<span data-ttu-id="d6381-121">De meest Ophalende functie over Hartree – Fock theorie is dat deze een Quantum status levert die geen entanglement tussen de electrons heeft.</span><span class="sxs-lookup"><span data-stu-id="d6381-121">The most striking feature about Hartree–Fock theory is that it yields a quantum state that has no entanglement between the electrons.</span></span>
<span data-ttu-id="d6381-122">Dit betekent dat het vaak een geschikte kwalitatieve beschrijving van de eigenschappen van moleculaire systemen bevat.</span><span class="sxs-lookup"><span data-stu-id="d6381-122">This means that it often provides a suitable qualitative description of properties of molecular systems.</span></span> 

<span data-ttu-id="d6381-123">De Hartree-Fock status kan ook van een `FermionHamiltonian`  als volgt worden samengesteld.</span><span class="sxs-lookup"><span data-stu-id="d6381-123">The Hartree-Fock state may also be reconstructed from a `FermionHamiltonian`  as follows.</span></span>
```csharp
// We initialize a fermion Hamiltonian.
var fermionHamiltonian = new FermionHamiltonian();

// Create a Hartree-Fock state from the Hamiltonian 
// with, say, `4` occupied spin orbitals.
var wavefunction = fermionHamiltonian.CreateHartreeFockState(nElectrons: 4);
```

<span data-ttu-id="d6381-124">Om nauw keurige resultaten te verkrijgen, met name voor sterk gecorreleerde systemen, moet u echter wel Quantum statussen hebben die verder gaan dan Hartree – Fock theorie.</span><span class="sxs-lookup"><span data-stu-id="d6381-124">However, obtaining accurate results, especially for strongly correlated systems, necessitate quantum states that go beyond Hartree–Fock theory.</span></span>
