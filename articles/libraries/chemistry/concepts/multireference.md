---
title: Gecorreleerde wavefunctions | Microsoft Docs
description: Quantum Dynamics conceptuele docs
author: guanghaolow
ms.author: gulow@microsoft.com
ms.date: 05/28/2019
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.multireference
ms.openlocfilehash: 0b14f373d31c5b63e313e07810daf62d9195b1d3
ms.sourcegitcommit: 8becfb03eb60ba205c670a634ff4daa8071bcd06
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/26/2019
ms.locfileid: "73184029"
---
# <a name="correlated-wavefunctions"></a><span data-ttu-id="53c1c-103">Gecorreleerde wavefunctions</span><span class="sxs-lookup"><span data-stu-id="53c1c-103">Correlated wavefunctions</span></span>

<span data-ttu-id="53c1c-104">Voor veel systemen, met name die in de buurt van de evenwichts geometrie, biedt [Hartree – Fock](xref:microsoft.quantum.chemistry.concepts.hartreefock) theorie een kwalitatieve beschrijving van de moleculaire eigenschappen via een verwijzings status met één determinant.</span><span class="sxs-lookup"><span data-stu-id="53c1c-104">For many systems, particularly those near the equilibrium geometry, [Hartree–Fock](xref:microsoft.quantum.chemistry.concepts.hartreefock) theory provides a qualitative description of molecular properties through a single-determinant reference state.</span></span> <span data-ttu-id="53c1c-105">Om een kwantitatieve nauw keurigheid te bereiken, moet u echter ook correlatie-effecten overwegen.</span><span class="sxs-lookup"><span data-stu-id="53c1c-105">However, in order to achieve quantitative accuracy, one must also consider correlation effects.</span></span> 

<span data-ttu-id="53c1c-106">In deze context is het belang rijk om te dinstinguishen tussen dynamische en niet-dynamische correlaties.</span><span class="sxs-lookup"><span data-stu-id="53c1c-106">In this context, it is important to dinstinguish between dynamic and non-dynamic correlations.</span></span>
<span data-ttu-id="53c1c-107">Dynamische correlaties ontstaan ten opzichte van de tendens van electrons om elkaar te blijven, zoals bij interelektronische repulsie.</span><span class="sxs-lookup"><span data-stu-id="53c1c-107">Dynamical correlations arise from the tendency of electrons to stay apart, such as due to interelectronic repulsion.</span></span> <span data-ttu-id="53c1c-108">Dit effect kan worden gemodelleerd door de electrons uit de referentie status te overwegen.</span><span class="sxs-lookup"><span data-stu-id="53c1c-108">This effect can be modelled by considering excitations of electrons out of the reference state.</span></span> <span data-ttu-id="53c1c-109">Niet-dynamische correlaties ontstaan wanneer de Wavefunction wordt gecentraliseerd door twee of meer configuraties op zeroth order, zelfs om alleen een kwalitatieve beschrijving van het systeem te krijgen.</span><span class="sxs-lookup"><span data-stu-id="53c1c-109">Non-dynamic correlations arise when the wavefunction is dominated by two or more configurations at zeroth order, even to achieve only a qualitative description of the system.</span></span>
<span data-ttu-id="53c1c-110">Dit vereist een superpositie van determinanten en is een voor beeld van een Wavefunction voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="53c1c-110">This necessitates a superposition of determinants and is an example of a multireference wavefunction.</span></span>

<span data-ttu-id="53c1c-111">De Library chemie biedt een manier om een zeroth-Wavefunction op te geven voor het probleem met meer verwijzingen als een superpositie van determinanten.</span><span class="sxs-lookup"><span data-stu-id="53c1c-111">The chemistry library provides a way to specify a zeroth order wavefunction for the multireference problem as a superposition of determinants.</span></span> <span data-ttu-id="53c1c-112">Deze methode, waarmee we sparse Multireference wavefunctions aanroepen, is effectief wanneer slechts enkele onderdelen voldoende zijn om de superpositie op te geven.</span><span class="sxs-lookup"><span data-stu-id="53c1c-112">This approach, which we call sparse multireference wavefunctions, is effective when only a few components suffice to specify the superposition.</span></span> <span data-ttu-id="53c1c-113">De bibliotheek biedt ook een methode voor het toevoegen van dynamische correlaties boven op een verwijzing naar één determinant via de gegeneraliseerde unitary gekoppelde-cluster Ansatz.</span><span class="sxs-lookup"><span data-stu-id="53c1c-113">The library also provides a method to include dynamic correlations on top of a single-determinant reference via the generalized unitary coupled-cluster ansatz.</span></span> <span data-ttu-id="53c1c-114">Daarnaast bouwt het ook Quantum circuits die deze statussen op een quantum computer genereren.</span><span class="sxs-lookup"><span data-stu-id="53c1c-114">Furthermore, it also constructs quantum circuits that generate these states on a quantum computer.</span></span> <span data-ttu-id="53c1c-115">Deze statussen kunnen worden opgegeven in het [Broombridge-schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge)en we bieden ook de functionaliteit om deze statussen hand matig op te geven via de Library chemie.</span><span class="sxs-lookup"><span data-stu-id="53c1c-115">These states may be specified in the [Broombridge schema](xref:microsoft.quantum.libraries.chemistry.schema.broombridge), and we also provide the functionality to manually specify these states through the chemistry library.</span></span>

## <a name="sparse-multi-reference-wavefunction"></a><span data-ttu-id="53c1c-116">Sparse multi-Reference Wavefunction</span><span class="sxs-lookup"><span data-stu-id="53c1c-116">Sparse multi-reference wavefunction</span></span>
<span data-ttu-id="53c1c-117">Een status met meerdere verwijzingen $ \ket{\psi_{\rm {MCSCF}} $ kan expliciet worden opgegeven als een lineaire combi natie van $N $-elektroas Slater determininants.</span><span class="sxs-lookup"><span data-stu-id="53c1c-117">A multi-reference state $\ket{\psi_{\rm {MCSCF}}}$ may be specified explicitly as a linear combination of $N$-electron Slater determininants.</span></span>
<span data-ttu-id="53c1c-118">\begin{align} \ket{\psi_{\rm {MCSCF}}} \propto \sum_{i_1 < i_2 < \cdots < i_N} \lambda_{i_1, i_2, \cdots, i_N} a ^ \dagger_{i_1}a ^ \dagger_{i_2}\cdots a ^ \dagger_{i_N}\ket{0}.</span><span class="sxs-lookup"><span data-stu-id="53c1c-118">\begin{align} \ket{\psi_{\rm {MCSCF}}} \propto \sum_{i_1 < i_2 < \cdots < i_N} \lambda_{i_1,i_2,\cdots,i_N} a^\dagger_{i_1}a^\dagger_{i_2}\cdots a^\dagger_{i_N}\ket{0}.</span></span>
<span data-ttu-id="53c1c-119">\end{align} bijvoorbeeld de status $ \propto (0.1 a ^ \dagger_1a ^ \dagger_2a ^ \dagger_6-0,2 a ^ \dagger_2a ^ \dagger_1a ^ \dagger_5) \ket{0}$ kan als volgt worden opgegeven in de Library chemie.</span><span class="sxs-lookup"><span data-stu-id="53c1c-119">\end{align} For example, the state $\propto(0.1 a^\dagger_1a^\dagger_2a^\dagger_6 - 0.2 a^\dagger_2a^\dagger_1a^\dagger_5)\ket{0}$ may be specified in the chemistry library as follows.</span></span>
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
<span data-ttu-id="53c1c-120">Deze expliciete weer gave van de superpositie onderdelen is effectief wanneer er slechts enkele onderdelen moeten worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="53c1c-120">This explicit representation of the superposition components is effective when only a few components need to be specified.</span></span> <span data-ttu-id="53c1c-121">Een voor beeld hiervan is het gebruik van deze representatie als er veel onderdelen nodig zijn om de gewenste status nauw keurig vast te leggen.</span><span class="sxs-lookup"><span data-stu-id="53c1c-121">One should avoid using this representation when many components are required to accurately capture the desired state.</span></span> <span data-ttu-id="53c1c-122">De reden hiervoor is de degelijkings kosten van het Quantum circuit waarmee deze status wordt voor bereid op een quantum computer, waarmee ten minste lineair wordt geschaald met het aantal superpositie onderdelen, en Maxi maal quadratically met de één norm van de amplitudes van de Super positie.</span><span class="sxs-lookup"><span data-stu-id="53c1c-122">The reason for this is the gate cost of quantum circuit that prepares this state on a quantum computer, which scales at least linearly with the number of superposition components, and at most quadratically with the one-norm of the superposition amplitudes.</span></span>

## <a name="unitary-coupled-cluster-wavefunction"></a><span data-ttu-id="53c1c-123">Unitary gekoppeld-cluster Wavefunction</span><span class="sxs-lookup"><span data-stu-id="53c1c-123">Unitary coupled-cluster wavefunction</span></span>
<span data-ttu-id="53c1c-124">Het is ook mogelijk om een unitary gekoppelde-cluster Wavefunction $ \ket{\psi_{\rm {UCC}}} $ op te geven met behulp van de chemistery-bibliotheek.</span><span class="sxs-lookup"><span data-stu-id="53c1c-124">It is also possible to specify a unitary coupled-cluster wavefunction $\ket{\psi_{\rm {UCC}}}$ using the chemistery library.</span></span> <span data-ttu-id="53c1c-125">In dit geval hebben we een verwijzings status met één determinant, zegt $ \ket{\psi_{\rm{SCF}}} $.</span><span class="sxs-lookup"><span data-stu-id="53c1c-125">In this situation, we have a single-determinant reference state, say, $\ket{\psi_{\rm{SCF}}}$.</span></span> <span data-ttu-id="53c1c-126">De onderdelen van de unitary gekoppelde cluster Wavefunction worden vervolgens impliciet opgegeven via een unitary-operator die wordt uitgevoerd op een referentie status.</span><span class="sxs-lookup"><span data-stu-id="53c1c-126">The components of the unitary coupled-cluster wavefunction are then specified implicity through a unitary operator acting on a reference state.</span></span>
<span data-ttu-id="53c1c-127">Deze unitary-operator wordt meestal geschreven als $e ^ {T-T ^ \dagger} $, waarbij $T-T ^ \dagger $ de anti-Hermitian-cluster operator is.</span><span class="sxs-lookup"><span data-stu-id="53c1c-127">This unitary operator is commonly written as $e^{T-T^\dagger}$, where $T-T^\dagger$ is the anti-Hermitian cluster operator.</span></span> <span data-ttu-id="53c1c-128">Daarom \begin{align} \ket{\psi_{\rm {UCC}}} = e ^ {T-T ^ \dagger}\ket{\psi_{\rm{SCF}}}.</span><span class="sxs-lookup"><span data-stu-id="53c1c-128">Thus \begin{align} \ket{\psi_{\rm {UCC}}} = e^{T-T^\dagger}\ket{\psi_{\rm{SCF}}}.</span></span>
<span data-ttu-id="53c1c-129">\end{align}</span><span class="sxs-lookup"><span data-stu-id="53c1c-129">\end{align}</span></span>

<span data-ttu-id="53c1c-130">Het is ook gebruikelijk om de cluster operator $T = T_1 + T_2 + \cdots $ te splitsen in delen, waarbij elk deel $T _J $ $j $-Body-termen bevat.</span><span class="sxs-lookup"><span data-stu-id="53c1c-130">It is also common to split the cluster operator $T = T_1 + T_2 + \cdots$ into parts, where each part $T_j$ contains $j$-body terms.</span></span> <span data-ttu-id="53c1c-131">In gegeneraliseerde gekoppelde cluster theorie heeft de cluster operator met één hoofd tekst (singles) de vorm \begin{align} T_1 = \sum_{pq}t ^ {p} _ {q} a ^ \dagger_p a_q, \end{align}</span><span class="sxs-lookup"><span data-stu-id="53c1c-131">In generalized coupled-cluster theory, the one-body cluster operator (singles) is of the form \begin{align} T_1 = \sum_{pq}t^{p}_{q} a^\dagger_p a_q, \end{align}</span></span>

<span data-ttu-id="53c1c-132">de cluster operator met twee hoofd tekst (dubbele) heeft de vorm \begin{align} T_2 = \sum_{pqrs}t ^ {pq} _ {RS} a ^ \dagger_p a ^ \dagger_q a_r a_s.</span><span class="sxs-lookup"><span data-stu-id="53c1c-132">and two-body cluster operator (doubles) is of the form \begin{align} T_2 = \sum_{pqrs}t^{pq}_{rs} a^\dagger_p a^\dagger_q a_r a_s.</span></span>
<span data-ttu-id="53c1c-133">\end{align}</span><span class="sxs-lookup"><span data-stu-id="53c1c-133">\end{align}</span></span>

<span data-ttu-id="53c1c-134">De voor waarden voor een hogere volg orde (drieën, 4, enzovoort) zijn mogelijk, maar worden momenteel niet ondersteund door de Library chemie.</span><span class="sxs-lookup"><span data-stu-id="53c1c-134">Higher-order terms (triples, quadruples, etc.) are possible, but not currently supported by the chemistry library.</span></span>

<span data-ttu-id="53c1c-135">Laat bijvoorbeeld $ \ket{\psi_{\rm{SCF}}} = a ^ \dagger_1 a ^ \dagger_2\ket{0}$ staan en laat $T = 0,123 a ^ \dagger_0 a_1 + 0,456 a ^ \dagger_0a ^ \dagger_3 a_1 a_2-0,789 a ^ \dagger_3a ^ \dagger_2 a_1 a_0 $.</span><span class="sxs-lookup"><span data-stu-id="53c1c-135">For example, let $\ket{\psi_{\rm{SCF}}} = a^\dagger_1 a^\dagger_2\ket{0}$, and let $T= 0.123 a^\dagger_0 a_1 + 0.456 a^\dagger_0a^\dagger_3 a_1 a_2 - 0.789 a^\dagger_3a^\dagger_2 a_1 a_0$.</span></span> <span data-ttu-id="53c1c-136">Vervolgens wordt deze status als volgt in de Library chemie geïnstantieerd.</span><span class="sxs-lookup"><span data-stu-id="53c1c-136">Then this state is instantiated in the chemistry library as follows.</span></span>
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

<span data-ttu-id="53c1c-137">Kring convervation kunnen expliciet worden gemaakt door `SpinOrbital` indices op te geven in plaats van een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="53c1c-137">Spin convervation may be made explicit by instead specifying `SpinOrbital` indices instead of integer indices.</span></span> <span data-ttu-id="53c1c-138">Laat bijvoorbeeld $ \ket{\psi_{\rm{SCF}}} = a ^ \dagger_{1, \uparrow} a ^ \dagger_{2, \downarrow}\ket{0}$, en laat $T = 0,123 a ^ \dagger_{0, \uparrow} a_ {1, \uparrow} + 0,456 a ^ \dagger_{0, \uparrow} a ^ \dagger_{3, \downarrow} a_ {1, \uparrow} a_ {2, \ downarrow}-0,789 a ^ \dagger_{3, \uparrow} a ^ \dagger_{2, \uparrow} a_ {1, \uparrow} a_ {0, \uparrow} $.</span><span class="sxs-lookup"><span data-stu-id="53c1c-138">For example, let $\ket{\psi_{\rm{SCF}}} = a^\dagger_{1,\uparrow} a^\dagger_{2, \downarrow}\ket{0}$, and let $T= 0.123 a^\dagger_{0, \uparrow} a_{1, \uparrow} + 0.456 a^\dagger_{0, \uparrow} a^\dagger_{3, \downarrow} a_{1, \uparrow} a_{2, \downarrow} - 0.789 a^\dagger_{3,\uparrow} a^\dagger_{2,\uparrow} a_{1,\uparrow} a_{0, \uparrow}$ be spin convserving.</span></span> <span data-ttu-id="53c1c-139">Vervolgens wordt deze status als volgt in de Library chemie geïnstantieerd.</span><span class="sxs-lookup"><span data-stu-id="53c1c-139">Then this state is instantiated in the chemistry library as follows.</span></span>
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

<span data-ttu-id="53c1c-140">We bieden ook een gebruiks vriendelijke functie die wordt gebruikt voor het opsommen van alle cluster operators met spin-conversaties die alleen geannihilatede spin-banen hebben en worden gehinderd op alleen onbezette spin-banen.</span><span class="sxs-lookup"><span data-stu-id="53c1c-140">We also provide a convenience function that enumerates over all spin-conversing cluster operators that annihilate only occupied spin-orbitals and excite to only unoccupied spin-orbitals.</span></span>
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