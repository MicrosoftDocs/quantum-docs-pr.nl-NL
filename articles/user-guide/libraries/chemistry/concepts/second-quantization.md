---
title: Tweede Kwantisatiefouten
description: Meer informatie over de tweede Kwantisatiefouten-benadering voor het model leren van elektronische structuren in kwantum programmering.
author: bradben
ms.author: v-benbra
ms.date: 10/09/2017
ms.topic: conceptual
uid: microsoft.quantum.chemistry.concepts.secondquantization
no-loc:
- Q#
- $$v
ms.openlocfilehash: a08e20d5b53aa97cb12ead0dc3a36069d0ec5df8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858839"
---
# <a name="second-quantization"></a><span data-ttu-id="bb432-103">Tweede Kwantisatiefouten</span><span class="sxs-lookup"><span data-stu-id="bb432-103">Second Quantization</span></span>

<span data-ttu-id="bb432-104">Tweede kwantisatiefouten kijkt naar het probleem van de elektronische structuur via een andere lens.</span><span class="sxs-lookup"><span data-stu-id="bb432-104">Second quantization looks at the problem of electronic structure through a different lens.</span></span>
<span data-ttu-id="bb432-105">In plaats van elke $N _e $ electrons toe te wijzen aan een specifieke staat (of Orbital), houdt tweede kwantisatiefouten elke Orbital bij en slaat het op of er in elk van deze elektron aanwezig zijn en tegelijkertijd de symmetrie-eigenschappen van de overeenkomstige functie van Wave worden gegarandeerd.</span><span class="sxs-lookup"><span data-stu-id="bb432-105">Rather than assigning each of the $N_e$ electrons to a specific state (or orbital), second quantization tracks each orbital and stores whether there is an electron present in each of them and at the same time automatically ensures symmetry properties of the corresponding wave function.</span></span>
<span data-ttu-id="bb432-106">Dit is belang rijk omdat het mogelijk is dat er quantum chemie-modellen worden opgegeven zonder dat u zich zorgen hoeft te maken over anti-symmetrizing de invoer status (zoals vereist voor fermions) en dat dergelijke modellen door de tweede kwantisatiefouten kunnen worden gesimuleerd met behulp van kleine quantum computers.</span><span class="sxs-lookup"><span data-stu-id="bb432-106">This is important because it allows quantum chemistry models to be specified without having to worry about anti-symmetrizing the input state (as is required for fermions) and also because second quantization allows such models to be simulated using small quantum computers.</span></span>

<span data-ttu-id="bb432-107">Als voor beeld van een tweede kwantisatiefouten in actie gaan we ervan uit dat $ \ psi_0 \cdots \ psi_ {N-1} $ een orthonormal-verzameling van ruimtelijke banen is.</span><span class="sxs-lookup"><span data-stu-id="bb432-107">As an example of second quantization in action, let's assume that $\psi_0\cdots \psi_{N-1}$ are an orthonormal set of spatial orbitals.</span></span>
<span data-ttu-id="bb432-108">Deze banen worden zo gekozen dat het systeem zo nauw keurig mogelijk kan worden weer gegeven binnen de beperkte basis die wordt overwogen.</span><span class="sxs-lookup"><span data-stu-id="bb432-108">These orbitals are chosen to represent the system as accurately as possible within the finite basis set considered.</span></span>
<span data-ttu-id="bb432-109">Een gemeen schappelijk voor beeld van deze banen is een Atomic-baan die een eigenbasis vormt voor de water stof Atom.</span><span class="sxs-lookup"><span data-stu-id="bb432-109">A common example of such orbitals are atomic orbitals which form an eigenbasis for the hydrogen atom.</span></span>
<span data-ttu-id="bb432-110">Omdat electrons twee statussen hebben, kan twee electrons worden Crammed in elk van deze ruimtelijke Orbital.</span><span class="sxs-lookup"><span data-stu-id="bb432-110">Because electrons have two spin states, two electrons can be crammed into each such spatial orbital.</span></span>
<span data-ttu-id="bb432-111">Dat wil zeggen dat de geldige basis statussen de volgende notatie hebben: $ \ psi_ {0, \uparrow}, \ldots, \ psi_ {N-1, \uparrow}, \ psi_ {0, \downarrow}, \ldots, \ psi_ {N-1, \downarrow} $, waarbij $ \uparrow $ en $ \downarrow $ de labels zijn die de twee eigenstates van de mate van vrijheid van de draaiing bepalen.</span><span class="sxs-lookup"><span data-stu-id="bb432-111">That is to say, the valid basis states are of the form $\psi_{0,\uparrow},\ldots,\psi_{N-1,\uparrow}, \psi_{0,\downarrow},\ldots,\psi_{N-1,\downarrow}$ where $\uparrow$ and $\downarrow$ are labels that specify the two eigenstates of the spin degree of freedom.</span></span>
<span data-ttu-id="bb432-112">Deze gecombineerde index van $ (j, \sigma) $ voor $ \sigma \in \{ \uparrow, \downarrow \} $ wordt ' spin-Orbital ' genoemd, omdat deze zowel de ruimtelijke als de mate van vrijheid van het niveau van de kring waarde bevat.</span><span class="sxs-lookup"><span data-stu-id="bb432-112">This combined index of $(j,\sigma)$ for $\sigma \in \{\uparrow,\downarrow\}$ is called a spin-orbital because it stores both the spatial as well as the spin degree of freedom.</span></span>
<span data-ttu-id="bb432-113">In de Library chemie worden spin-banen opgeslagen in een `SpinOrbital` gegevens structuur en als volgt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="bb432-113">In the chemistry library, spin-orbitals are stored in a `SpinOrbital` data structure, and are created as follows.</span></span>

```csharp
    // First, we load the namespace containing spin-orbital objects.
    using Microsoft.Quantum.Chemistry.OrbitalIntegrals;

    // First, we assign an orbital index, say `5`. Note that we use 0-indexing,
    // so this is the 6th orbital.
    var orbitalIdx = 5;

    // Second, we assign a spin index, say `Spin.u` for spin up or `Spin.d` for spin down.
    var spin = Spin.d;

    // the spin-orbital (5, ↓) is then
    var spinOrbital = new SpinOrbital(orbitalIdx, spin);

    // A tuple `(int, Spin)` is also implicitly recognized as a spin-orbital.
    (int, Spin) tuple = (orbitalIdx, spin);

    // We explicitly specify the type of `spinOrbital1` to demonstrate
    // the implicit cast to `SpinOrbital`.
    SpinOrbital spinOrbital1 = tuple;
```

<span data-ttu-id="bb432-114">Dit betekent dat we formeel kunnen nadenken over het spin en ruimtelijke deel van de functie Wave als $ \ psi_ {0} \cdots \ psi_ {2n-1} $, waarbij elk van de indices nu een opsomming is van een $ (j, \sigma) $.</span><span class="sxs-lookup"><span data-stu-id="bb432-114">This means that we can formally think of the basis for both the spin and spatial part of the wave function as $\psi_{0} \cdots \psi_{2N-1}$ where each of the indices now is an enumeration of a $(j,\sigma)$.</span></span>
<span data-ttu-id="bb432-115">Een mogelijke opsomming is $g (j, \sigma) = j + N\sigma ' $.</span><span class="sxs-lookup"><span data-stu-id="bb432-115">One possible enumeration is $g(j,\sigma) = j+N\sigma'$.</span></span>
<span data-ttu-id="bb432-116">Een andere mogelijke opsomming is $h (j, \sigma) = 2 \* j + \sigma $.</span><span class="sxs-lookup"><span data-stu-id="bb432-116">Another possible enumeration is $h(j,\sigma) = 2\*j + \sigma$.</span></span>
<span data-ttu-id="bb432-117">De quantum chemie-bibliotheek kan gebruikmaken van deze conventies en de spin-banen in een dergelijke code ring kunnen als volgt worden geïnstantieerd.</span><span class="sxs-lookup"><span data-stu-id="bb432-117">The quantum chemistry library can use these conventions, and the spin-orbitals in such an encoding can be instantiated as follows.</span></span>

```csharp
    // Let us use the spin orbital created in the previous snippet.
   var spinOrbital = new SpinOrbital(5, Spin.d);

   // Let us set the total number of orbitals to be say, `7`.
   var nOrbitals = 7;

    // This converts a spin-orbital index to a unique integer, in this case `12`,
    // using the formula `g(j,σ)`.
    var integerIndexHalfUp = spinOrbital.ToInt(IndexConvention.HalfUp);

    // This converts a spin-orbital index to a unique integer, in this case `11`,
    // using the formula `h(j,σ)`.
    var integerIndexUpDown = spinOrbital.ToInt(IndexConvention.UpDown);

    // The default conversion uses the formula `h(j,σ)`, in this case `11`.
    var integerIndexDefault = spinOrbital.ToInt();
```

<span data-ttu-id="bb432-118">Voor fermionic-systemen wordt voor komen dat er meer dan één elektro uren aanwezig zijn in een spin-Orbital tegelijk.</span><span class="sxs-lookup"><span data-stu-id="bb432-118">For fermionic systems, the Pauli exclusion principle prevents more than one electron from being present in any spin-orbital at the same time.</span></span>
<span data-ttu-id="bb432-119">Dit betekent dat we de twee juridische Staten kunnen schrijven voor $ \ psi_1 $ als \begin{Equation} \ psi_1 \rightarrow \begin{cases} \ket {0} _1 & \Text{if $ \ psi_1 $ niet bezet is,} </span><span class="sxs-lookup"><span data-stu-id="bb432-119">This means that we can write the two legal states for $\psi_1$ as \begin{equation} \psi_1 \rightarrow \begin{cases} \ket{0}_1 & \text{if $\psi_1$ is not occupied,} </span></span>\\\
<span data-ttu-id="bb432-120">\ket {1} _1 & \Text{if $ \ psi_1 $ is bezet.}</span><span class="sxs-lookup"><span data-stu-id="bb432-120">\ket{1}_1 & \text{if $\psi_1$ is occupied.}</span></span> <span data-ttu-id="bb432-121">\end{cases} \end{Equation} deze code ring is ideaal voor quantum computers, omdat het elektronische beroep als één Quantum bit kan worden opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="bb432-121">\end{cases} \end{equation} This encoding is great for quantum computers because it means that we can store the electronic occupation as a single quantum bit.</span></span>

<span data-ttu-id="bb432-122">De beroeps statussen voor de $2N $ spin-banen kunnen op dezelfde manier worden opgeslagen in $2N $ qubits.</span><span class="sxs-lookup"><span data-stu-id="bb432-122">The occupation states for the $2N$ spin orbitals can similarly be stored in $2N$ qubits.</span></span>
<span data-ttu-id="bb432-123">Als $N bijvoorbeeld = $2, is de status $ $ \ket {0} \ket {1} \ket {1} \ket {0} , $ $</span><span class="sxs-lookup"><span data-stu-id="bb432-123">As an example, if $N=2$ then the state $$ \ket{0} \ket{1} \ket{1} \ket{0}, $$</span></span>

<span data-ttu-id="bb432-124">komt overeen met de kring velden $1 $ en $2 $ die worden ingen Omen met de rest lege.</span><span class="sxs-lookup"><span data-stu-id="bb432-124">would correspond to spin orbitals $1$ and $2$ being occupied with the remainder empty.</span></span>
<span data-ttu-id="bb432-125">Op dezelfde manier is de status $ $ \ket {0} \equiv \ket {0} _{0} {0} \cdots \ket_{N-1}, $ $</span><span class="sxs-lookup"><span data-stu-id="bb432-125">Similarly, the state $$ \ket{0} \equiv \ket{0}_{0} \cdots \ket{0}_{N-1}, $$</span></span>

<span data-ttu-id="bb432-126">heeft geen electrons en wordt aangeduid als ' vacuüm status '.</span><span class="sxs-lookup"><span data-stu-id="bb432-126">has no electrons and is known as the 'vacuum state'.</span></span>

<span data-ttu-id="bb432-127">Een prachtige kant van het tweede kwantisatiefouten is dat we de anti-symmetrie van de Quantum status niet langer hoeven te volgen.</span><span class="sxs-lookup"><span data-stu-id="bb432-127">A beautiful side-effect of second quantization is that we no longer have to explicitly keep track of the anti-symmetry of the quantum state.</span></span>
<span data-ttu-id="bb432-128">Dit komt omdat de anti-symmetrie van de staat zichzelf voordoet, in plaats van de anti-werk regels van de Opera tors die elektronische beroepen van een spin Orbital maken en vernietigen.</span><span class="sxs-lookup"><span data-stu-id="bb432-128">This is because, as we will see, the anti-symmetry of the state represents itself instead through the anti-commutation rules of the operators that create and destroy electronic occupations of a spin orbital.</span></span>

## <a name="fermionic-operators"></a><span data-ttu-id="bb432-129">Fermionic-Opera tors</span><span class="sxs-lookup"><span data-stu-id="bb432-129">Fermionic operators</span></span>

<span data-ttu-id="bb432-130">De twee fundamentele Opera tors die op de secundaire basis vectoren handelen, worden het maken en Annihilation Opera tors genoemd.</span><span class="sxs-lookup"><span data-stu-id="bb432-130">The two fundamental operators that act on the second-quantized basis vectors are known as creation and annihilation operators.</span></span>
<span data-ttu-id="bb432-131">Deze opera tors invoegen of vernietigen electrons op een bepaalde locatie.</span><span class="sxs-lookup"><span data-stu-id="bb432-131">These operators insert or destroy electrons at a particular location.</span></span>
<span data-ttu-id="bb432-132">Deze worden aangeduid $a ^ \ dagger_j $ en $a _j $ respectievelijk.</span><span class="sxs-lookup"><span data-stu-id="bb432-132">These are denoted $a^\dagger_j$ and $a_j$ respectively.</span></span>

<span data-ttu-id="bb432-133">Bijvoorbeeld \begin{align} a ^ \ dagger_1 \ket {0} _1 = \ket {1} _1, \quad a ^ \ dagger_1 \ket {1} _1 = 0, \quad a_1 \ket {0} _1 = 0, \quad a_1 \ket {1} _1 = \ket {0} _1.</span><span class="sxs-lookup"><span data-stu-id="bb432-133">For example, \begin{align} a^\dagger_1 \ket{0}_1 = \ket{1}_1,\quad a^\dagger_1 \ket{1}_1 = 0,\quad a_1 \ket{0}_1 = 0,\quad a_1 \ket{1}_1 = \ket{0}_1.</span></span>
<span data-ttu-id="bb432-134">in \end{align} ziet u dat hier $a ^ \ dagger_1 \ket {1} _1 = 0 $ en $a _1 \ket {0} _1 $ resulteert in de nul-vector, niet $ \ket {0} _1 $.</span><span class="sxs-lookup"><span data-stu-id="bb432-134">\end{align} Note that here $a^\dagger_1 \ket{1}_1=0$ and $a_1 \ket{0}_1$ yield the zero-vector not $\ket{0}_1$.</span></span>
<span data-ttu-id="bb432-135">Dergelijke Opera tors zijn daarom noch Hermitian noch unitary.</span><span class="sxs-lookup"><span data-stu-id="bb432-135">Such operators are therefore neither Hermitian nor unitary.</span></span>
<span data-ttu-id="bb432-136">De Opera tors voor algemeen maken en Annihilation worden aangeduid met het <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderOperator`1> type.</span><span class="sxs-lookup"><span data-stu-id="bb432-136">We represent general creation and annihilation operators using the <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderOperator`1> type.</span></span>
<span data-ttu-id="bb432-137">Een enkele operator voor maken wordt bijvoorbeeld als volgt weer gegeven.</span><span class="sxs-lookup"><span data-stu-id="bb432-137">For instance, a single creation operator is represented as follow.</span></span>

```csharp
    // We load the namespace containing ladder operator objects.
    using Microsoft.Quantum.Chemistry.LadderOperators;

    // Let us use the spin orbital created in the previous snippet.
    var spinOrbitalInteger = new SpinOrbital(5, Spin.d).ToInt();

    // We specify either a creation or annihilation operator using 
    // the enumerable type `RaisingLowering.u` or `RaisingLowering.d`
    // respectively;
    var creationEnum = RaisingLowering.u;

    // The type representing a creation operator is then initialized 
    // as follows. Here, we index these operators with integers.
    // Hence we initialize the generic ladder operator with an
    // integer index type.
    var ladderOperator0 = new LadderOperator<int>(creationEnum, spinOrbitalInteger);

    // An alternate constructor for a LadderOperator instead uses
    // a tuple.
    var ladderOperator1 = new LadderOperator<int>((creationEnum, spinOrbitalInteger));
```

<span data-ttu-id="bb432-138">Met behulp van dergelijke Opera tors kunnen we ook \ket {0} \ket {1} \ket {1} \ket {0} = a ^ \ dagger_1 een ^ \ dagger_2 \ket {0} ^ {\otimes 4}.</span><span class="sxs-lookup"><span data-stu-id="bb432-138">Also using such operators we can express $$ \ket{0} \ket{1} \ket{1} \ket{0} = a^\dagger_1 a^\dagger_2 \ket{0}^{\otimes 4}.</span></span>
<span data-ttu-id="bb432-139">$ $ Deze volg orde van Opera tors wordt in de Hamiltonian-simulatie bibliotheek gemaakt met behulp van C#-code die vergelijkbaar is met de Orbital-situatie met één spin die hierboven wordt behandeld:</span><span class="sxs-lookup"><span data-stu-id="bb432-139">$$ This sequence of operators would be constructed within the Hamiltonian simulation library using C# code that is similar to the single-spin orbital case considered above above:</span></span>
```csharp
    // We load the namespace containing fermion-related objects.
    using Microsoft.Quantum.Chemistry.Fermion;

    // Let us initialize an array of tuples representing the
    // desired sequence of creation operators.
    var indices = new[] { (RaisingLowering.u, 1), (RaisingLowering.u, 2) };

    // We can convert this array of tuples to a sequence of ladder
    // operators using the `ToLadderSequence()` methods.
    var ladderSequences = indices.ToLadderSequence();

    // Sequences of ladder operators are quite general. For instance,
    // they could be bosonic operators, instead of fermionic operators.
    // We specialize them by constructing a `FermionTerm` representing 
    // a fermion creation operator on the index `2` followed by `1`.
    var fermionTerm = new FermionTerm(ladderSequences);
```

<span data-ttu-id="bb432-140">Voor een systeem van $k $ Fermions, in de tweede kwantisatiefouten is de actie van de operator maken $a ^ \ dagger_i $ gegeven door $ $ a ^ \ dagger_i \ket{n_1, n_2, \ldots, 0_i, \ldots, n_k} = (-1) ^ {S_i} \ket{n_1, n_2, \ldots, 1_i, \ldots, n_k}, $ $ en $ $ a ^ \ dagger_i \ket{n_1, n_2, \ldots, 1_i, \ldots, n_k} = 0, $ $ waar $S _i = \ sum_ {j<i} a ^ \ dagger_j a_j $ meet het totale aantal Fermions dat in de staat van één partikel is en die een index heeft $j < i $.</span><span class="sxs-lookup"><span data-stu-id="bb432-140">For a system of $k$ Fermions, in second quantization the action of the creation operator $a^\dagger_i$ is given by $$ a^\dagger_i \ket{n_1, n_2, \ldots, 0_i, \ldots, n_k } = (-1)^{S_i} \ket{n_1, n_2, \ldots, 1_i, \ldots, n_k}, $$ and $$ a^\dagger_i \ket{n_1, n_2, \ldots, 1_i, \ldots, n_k } = 0, $$ where $S_i = \sum_{j<i} a^\dagger_j a_j$ measures the total number of Fermions that are in the state of a single particle and that have an index $j < i$.</span></span>

<span data-ttu-id="bb432-141">Een derde operator wordt ook vaak gebruikt in tweede verdeelde representaties.</span><span class="sxs-lookup"><span data-stu-id="bb432-141">A third operator is also often used in second quantized representations.</span></span>
<span data-ttu-id="bb432-142">Deze operator staat bekend als de operator Number en wordt gedefinieerd door \begin{Equation} n_i = a ^ \ dagger_i a_i.</span><span class="sxs-lookup"><span data-stu-id="bb432-142">This operator is known as the number operator and is defined by \begin{equation} n_i = a^\dagger_i a_i.</span></span>
<span data-ttu-id="bb432-143">\end{Equation} deze operator telt het beroep van een gegeven Orbital, wat wil zeggen \begin{align} n_i \ket {0} _i &= 0 \ geen getal</span><span class="sxs-lookup"><span data-stu-id="bb432-143">\end{equation} This operator counts the occupation of a given spin orbital, which is to say \begin{align} n_i \ket{0}_i &= 0\nonumber</span></span>\\\
<span data-ttu-id="bb432-144">n_i \ket {1} _i &= \ket {1} _I.</span><span class="sxs-lookup"><span data-stu-id="bb432-144">n_i \ket{1}_i &= \ket{1}_i.</span></span>
<span data-ttu-id="bb432-145">\end{align} die vergelijkbaar zijn met de bovenstaande `FermionTerm` voor beelden, is deze nummer operator als volgt samengesteld.</span><span class="sxs-lookup"><span data-stu-id="bb432-145">\end{align} Similar to the above `FermionTerm` examples, this number operator is constructed as follows.</span></span>
```csharp
    // Let us use a new method to compactly create a sequence of ladder
    // operators. Note that we have omitted specifying whether the 
    // operators are raising or lowering. In this case, the first half
    // will be raising operators, and the second half will be lowering 
    // operators.
    var indices = new[] { 1, 1 }.ToLadderSequence();

    // We now construct a `FermionTerm` representing an annihilation operator
    // on the index 1 followed by the creation operator on the index 1.
    var fermionTerm0 = new FermionTerm(indices);
```

<span data-ttu-id="bb432-146">Er komt een subtlety bij het gebruik van de Opera tors maken of Annihilation in fermionic-systemen.</span><span class="sxs-lookup"><span data-stu-id="bb432-146">A subtlety emerges though when using creation or annihilation operators in fermionic systems.</span></span>
<span data-ttu-id="bb432-147">Een geldige Quantum staat is niet-symmetrisch onder uitwisseling van labels.</span><span class="sxs-lookup"><span data-stu-id="bb432-147">We require that any valid quantum state is anti-symmetric under exchange of labels.</span></span>
<span data-ttu-id="bb432-148">Dit betekent dat $ $ a ^ \ dagger_2 een ^ \ dagger_1 \ket {0} =-a ^ \ dagger_1 een ^ \ dagger_2 \ket {0} .</span><span class="sxs-lookup"><span data-stu-id="bb432-148">This means that $$ a^\dagger_2 a^\dagger_1 \ket{0} = -a^\dagger_1 a^\dagger_2 \ket{0}.</span></span>
<span data-ttu-id="bb432-149">$ $ Dergelijke Opera tors zijn "antiwerkend" en in het algemeen voor elke $i, j $ we hebben dat \begin{align} een ^ \ dagger_i een ^ \ dagger_j =-(1-\ delta_ {i, j}) een ^ \ dagger_j een ^ \ dagger_i, \quad a ^ \ dagger_i a_j = \ delta_ {i, j}-a_j een ^ \ dagger_i.</span><span class="sxs-lookup"><span data-stu-id="bb432-149">$$ Such operators are said to 'anti-commute' and in general for any $i, j$ we have that \begin{align} a^\dagger_i a^\dagger_j  = -(1-\delta_{i,j})a^\dagger_j a^\dagger_i,\quad a^\dagger_i a_j =\delta_{i,j} - a_j a^\dagger_i.</span></span>
<span data-ttu-id="bb432-150">\end{align} dus de volgende twee <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderSequence`1> instanties worden beschouwd als een gelijkwaardige waarde</span><span class="sxs-lookup"><span data-stu-id="bb432-150">\end{align} Thus the following two <xref:Microsoft.Quantum.Chemistry.LadderOperators.LadderSequence`1> instances are considered inequivalent</span></span>
```csharp
    // Let us initialize an array of tuples representing the
    // desired sequence of creation operators.
    var indices = new[] { (RaisingLowering.u, 1), (RaisingLowering.u, 2) };

    // We now construct a `LadderSequence` representing a creation operator
    // on the index 1 followed by 2, then a term with the reverse ordering.
    var laddderSeqeunce = indices.ToLadderSequence();
    var laddderSeqeunceReversed = indices.Reverse().ToLadderSequence();

    // The following Boolean is `false`.
    var equal = laddderSeqeunce == laddderSeqeunceReversed;
```

<span data-ttu-id="bb432-151">De vereiste dat elk van de verwerkings exploitanten antiwerkers betekent dat het gebruik van een tweede gevormde vertegenwoordiging verstrekken de uitdagingen van de anti-symmetrie van Fermions.</span><span class="sxs-lookup"><span data-stu-id="bb432-151">The requirement that each of the creation operators anti-commute means that using a second quantized representation does obviate the challenges faced by the anti-symmetry of Fermions.</span></span>
<span data-ttu-id="bb432-152">In plaats daarvan wordt de uitdaging in de definitie van de Opera tors voor maken hersteld.</span><span class="sxs-lookup"><span data-stu-id="bb432-152">Instead the challenge re-emerges in our definition of the creation operators.</span></span> 

<span data-ttu-id="bb432-153">Bij het gebruik van de regels voor anti-werkingen `LadderSequence` komen sommige instanties in werkelijkheid overeen met dezelfde volg orde van fermionic-Opera Tors, soms met een minteken.</span><span class="sxs-lookup"><span data-stu-id="bb432-153">Using the anti-commutation rules, some `LadderSequence` instances actually correspond to the same sequence of fermionic operators, sometimes up to a minus sign.</span></span>
<span data-ttu-id="bb432-154">Denk bijvoorbeeld aan de Hamiltonian $a _0 ^ \dagger a_1 ^ \dagger a_1 a_0 =-a_1 ^ \dagger a_0 ^ \dagger a_1 a_0 $.</span><span class="sxs-lookup"><span data-stu-id="bb432-154">For instance, consider the Hamiltonian $a_0^\dagger a_1^\dagger a_1 a_0 = - a_1^\dagger a_0^\dagger a_1 a_0$.</span></span>
<span data-ttu-id="bb432-155">Hiermee wordt ons gemotiveren een canonieke ordening voor elke te definiëren `FermionTerm` .</span><span class="sxs-lookup"><span data-stu-id="bb432-155">This motivates us to define a canonical ordering for every `FermionTerm`.</span></span>
<span data-ttu-id="bb432-156">Elk `FermionTerm` wordt automatisch als volgt in canonieke volg orde geplaatst.</span><span class="sxs-lookup"><span data-stu-id="bb432-156">Any `FermionTerm` is automatically put into canonical order as follows.</span></span>
```csharp
    // We now construct two `FermionTerms` that are equivalent with respect to
    // anti-commutation up to a sign change.
    var fermionTerm0 = new FermionTerm(new[] { 0, 1, 1, 0 }.ToLadderSequence());
    var fermionTerm1 = new FermionTerm(new[] { 1, 0, 1, 0 }.ToLadderSequence());

    // The following Boolean is `true`.
    var sequenceEqual = fermionTerm0 == fermionTerm1;

    // The change in sign is not compared above, but is an internally tracked
    // property of `FermionTerm`.
    int sign0 = fermionTerm0.Coefficient;
    var sign1 = fermionTerm1.Coefficient;

    // The following Boolean is `false`.
    var signEqual = sign0 == sign1;
```

## <a name="second-quantized-fermionic-hamiltonian"></a><span data-ttu-id="bb432-157">Second-Quantized Fermionic Hamiltonian</span><span class="sxs-lookup"><span data-stu-id="bb432-157">Second-Quantized Fermionic Hamiltonian</span></span>

<span data-ttu-id="bb432-158">Het is misschien unsurprising dat de Hamiltonian in [Quantum modellen voor elektronische systemen](xref:microsoft.quantum.chemistry.concepts.quantummodels) kan worden geschreven in termen van maken en Annihilation-Opera tors.</span><span class="sxs-lookup"><span data-stu-id="bb432-158">It is perhaps unsurprising that the Hamiltonian in [Quantum Models for Electronic Systems](xref:microsoft.quantum.chemistry.concepts.quantummodels) can be written in terms of creation and annihilation operators.</span></span>
<span data-ttu-id="bb432-159">Met name als $ \psi \_ j $ de kring banen zijn die de basis vormen, dan</span><span class="sxs-lookup"><span data-stu-id="bb432-159">In particular, if $\psi\_j$ are the spin orbitals that form the basis then</span></span>

<span data-ttu-id="bb432-160">\begin{Equation} \hat{H} = \sum \_ {pq} H \_ {pq} a ^ \dagger \_ p a \_ q + \frac {1} {2} \sum \_ {pqrs} H \_ {pqrs} a ^ \dagger \_ p a ^ \dagger \_ q a \_ Ra \_ s + H \_ {\textrm NUC}, \label{EQ: totalHam} \end{Equation}, waarbij $h \_ {\textrm NUC} $ de kern energie is (een constante onder de Born-Oppenheimer benadering) en</span><span class="sxs-lookup"><span data-stu-id="bb432-160">\begin{equation} \hat{H} = \sum\_{pq} h\_{pq}a^\dagger\_p a\_q + \frac{1}{2}\sum\_{pqrs} h\_{pqrs}a^\dagger\_p a^\dagger\_q a\_ra\_s +h\_{\textrm nuc},\label{eq:totalHam} \end{equation} where $h\_{\textrm nuc}$ is the nuclear energy (which is a constant under the Born-Oppenheimer approximation) and</span></span>

<span data-ttu-id="bb432-161">\begin{align} h \_ {pq} &= \int \_ {-\infty} ^ \infty \psi ^ \* \_ p (x \_ 1) \left (-\Frac{\nabla ^ 2} {2} + V (x \_ 1) \right) \psi \_ q (x \_ 1) \mathrm{d} ^ 3x \_ 1, \end{align}</span><span class="sxs-lookup"><span data-stu-id="bb432-161">\begin{align} h\_{pq} &= \int\_{-\infty}^\infty \psi^\*\_p(x\_1) \left(-\frac{\nabla^2}{2} +V(x\_1)\right)  \psi\_q(x\_1)\mathrm{d}^3x\_1, \end{align}</span></span>

<span data-ttu-id="bb432-162">waarbij $V (x) $ het potentieel veld is, en</span><span class="sxs-lookup"><span data-stu-id="bb432-162">where $V(x)$ is the mean-field potential, and</span></span>

<span data-ttu-id="bb432-163">\begin{align} h \_ {pqrs} &= \int \_ {-\infty} ^ \infty \int \_ {-\infty} ^ \infty\psi \_ p ^ \* (x \_ 1) \psi \_ q ^ \* (x \_ 2) \left (\frac {1} {| x_1-x_2 |} \right) \psi \_ r (x \_ 2) \psi \_ s (x \_ 1) \mathrm{d} ^ 3x \_ 1 \ mathrm {d} ^ 3x \_ 2. \ label {EQ: integralen} \end{align}</span><span class="sxs-lookup"><span data-stu-id="bb432-163">\begin{align} h\_{pqrs} &= \int\_{-\infty}^\infty \int\_{-\infty}^\infty\psi\_p^\*(x\_1)\psi\_q^\*(x\_2) \left(\frac{1}{|x_1-x_2|} \right)\psi\_r(x\_2)\psi\_s(x\_1)\mathrm{d}^3x\_1\mathrm{d}^3x\_2.\label{eq:integrals} \end{align}</span></span>

<span data-ttu-id="bb432-164">De voor waarden $h \_ {pq} $ worden aangeduid als een-, integrale integraal, omdat al deze voor waarden slechts één electrons omvatten en ook $h \_ {pqrs} $ de twee-elektroden integraal zijn.</span><span class="sxs-lookup"><span data-stu-id="bb432-164">The terms $h\_{pq}$ are referred to as one-electron integrals because all such terms only involve single electrons and likewise $h\_{pqrs}$ are the two-electron integrals.</span></span>
<span data-ttu-id="bb432-165">Ze worden integralen genoemd, omdat het berekenen van de waarden van deze coëfficiënten een integraal vereist.</span><span class="sxs-lookup"><span data-stu-id="bb432-165">They are called integrals because computing the values of these coefficients requires an integral.</span></span>
<span data-ttu-id="bb432-166">De één elektroon-term beschrijft de kinetische energie van de afzonderlijke electrons en hun interacties met de elektrische velden van de kernen.</span><span class="sxs-lookup"><span data-stu-id="bb432-166">The one electron terms describe the kinetic energy of the individual electrons and their interactions with the electric fields of the nuclei.</span></span>
<span data-ttu-id="bb432-167">De twee-elektroden integralen anderzijds beschrijven de interacties tussen de electrons.</span><span class="sxs-lookup"><span data-stu-id="bb432-167">The two-electron integrals on the other hand describe the interactions between the electrons.</span></span>

<span data-ttu-id="bb432-168">Een Intuition voor wat deze termen betekenen, kan afgelezen zijn van de Opera tors maken en Annihilation die elk daarvan bestaan.</span><span class="sxs-lookup"><span data-stu-id="bb432-168">An intuition for what these terms mean can be gleaned from the creation and annihilation operators that comprise each of them.</span></span>
<span data-ttu-id="bb432-169">Bijvoorbeeld, $h _ {pq} a ^ \ dagger_p a_q $ beschrijft de elektron verspringen van Orbital $q $ om Orbital $p $ te draaien.</span><span class="sxs-lookup"><span data-stu-id="bb432-169">For example, $h_{pq}a^\dagger_p a_q$ describes the electron hopping from spin orbital $q$ to spin orbital $p$.</span></span>
<span data-ttu-id="bb432-170">Op dezelfde manier worden met de term $h _ {pqrs} a ^ \ dagger_p een ^ \ dagger_q a_r a_s $ (voor DISTINCT $p, q, r, s $) twee electrons in kring velden $r $ en $s $-sprei ding van elkaar beschreven en eindigend op spin banen $p $ en $q $.</span><span class="sxs-lookup"><span data-stu-id="bb432-170">Similarly, the term $h_{pqrs} a^\dagger_p a^\dagger_q a_r a_s$ (for distinct $p,q,r,s$) describes two electrons in spin orbitals $r$ and $s$ scattering off of each other and ending up in spin orbitals $p$ and $q$.</span></span>
<span data-ttu-id="bb432-171">Als $r = q $ en $p = s $ then $h _ {prrp} a ^ \ dagger_p een ^ \ dagger_r a_r a_p = h_ {prrp} n_p n_r $ de energie boete van de twee electrons bijna op elkaar lijkt, maar beschrijft geen dynamisch proces.</span><span class="sxs-lookup"><span data-stu-id="bb432-171">If $r=q$ and $p=s$ then $h_{prrp} a^\dagger_p a^\dagger_r a_r a_p = h_{prrp} n_p n_r$ gives the energy penalty associated with the two electrons being near each other, but does not describe a dynamical process.</span></span>

<span data-ttu-id="bb432-172">We kunnen dergelijke Hamiltonians met behulp van de `FermionHamiltonian` -klasse vertegenwoordigen. Dit is in feite een lijst die alle gewenste `FermionTerm` instanties bevat.</span><span class="sxs-lookup"><span data-stu-id="bb432-172">We may represent such Hamiltonians using the `FermionHamiltonian` class, which is essentially a list containing all the desired `FermionTerm` instances.</span></span>
<span data-ttu-id="bb432-173">Als Hamiltonians worden Hermitian per definitie, indexeren we termen met het complexere type `HermitianFermionTerm` dat ook Hermitian symmetrie gebruikt bij het controleren of de voor waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="bb432-173">As Hamiltonians are Hermitian by definition, we index terms using the more specialized type `HermitianFermionTerm` that also uses Hermitian symmetry when checking whether terms are equivalent.</span></span>

<span data-ttu-id="bb432-174">Laat ons enkele voor beelden van een voor beeld maken.</span><span class="sxs-lookup"><span data-stu-id="bb432-174">Let us construct a few illustrative examples.</span></span>
<span data-ttu-id="bb432-175">Bekijk de Hamiltonian $ \hat{H} = a_0 ^ \dagger a_1 + a_1 ^ \dagger a_0 $.</span><span class="sxs-lookup"><span data-stu-id="bb432-175">Consider the Hamiltonian $\hat{H} = a_0^\dagger a_1 + a_1^\dagger a_0$.</span></span>
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We construct the terms to be added.
    var fermionTerm0 = new FermionTerm(new[] { 1, 0 }.ToLadderSequence());
    var fermionTerm1 = new FermionTerm(new[] { 0, 1 }.ToLadderSequence());

    // These fermion terms are not equal. The following Boolean is `false`.
    var sequenceEqual = fermionTerm0 == fermionTerm1;

    // However, these terms are equal under Hermitian symmetry.
    // We also take the opportunity to demonstrate equivalent constructors
    // for hermitian fermion terms
    var hermitianFermionTerm0 = new HermitianFermionTerm(fermionTerm0);
    var hermitianFermionTerm1 = new HermitianFermionTerm(new[] { 0, 1 });

    // These Hermitian fermion terms are equal. The following Boolean is `true`.
    var hermitianSequenceEqual = hermitianFermionTerm0 == hermitianFermionTerm1;

    // We add the terms to the Hamiltonian with the appropriate coefficient.
    // Note that these terms are identical.
    hamiltonian.Add(hermitianFermionTerm0, 1.0);
    hamiltonian.Add(hermitianFermionTerm1, 1.0);
```
<span data-ttu-id="bb432-176">We kunnen deze constructie vereenvoudigen met het feit dat Hamiltonian Opera tors van Hermitian zijn.</span><span class="sxs-lookup"><span data-stu-id="bb432-176">We may simplify this construction using the fact that Hamiltonian operators are Hermitian operators.</span></span>
<span data-ttu-id="bb432-177">Wanneer u voor waarden toevoegt aan de Hamiltonian met `Add` , wordt ervan uitgegaan dat de niet-Hermitian-term bijvoorbeeld `fermionTerm0` wordt gekoppeld aan de bijbehorende Hermitian geconjugeerde.</span><span class="sxs-lookup"><span data-stu-id="bb432-177">When adding terms to the Hamiltonian using `Add`, any non-Hermitian term such as `fermionTerm0` is assumed to be paired with its Hermitian conjugate.</span></span>
<span data-ttu-id="bb432-178">Het volgende code fragment bevat dus ook dezelfde Hamiltonian:</span><span class="sxs-lookup"><span data-stu-id="bb432-178">Thus the following snippet also represents the same Hamiltonian:</span></span>
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We construct the term to be added -- note the doubled coefficient.
    hamiltonian.Add(new HermitianFermionTerm(new[] { 1, 0 }), 2.0);
```

<span data-ttu-id="bb432-179">Door gebruik te maken van de regels voor anti-werkingen, `FermionTerm` komen sommige instanties in de Hamiltonian in werkelijkheid overeen met dezelfde volg orde van fermionic-Opera Tors, soms met een minteken.</span><span class="sxs-lookup"><span data-stu-id="bb432-179">Using the anti-commutation rules, some `FermionTerm` instances in the Hamiltonian actually correspond to the same sequence of fermionic operators, sometimes up to a minus sign.</span></span>
<span data-ttu-id="bb432-180">Denk bijvoorbeeld aan de Hamiltonian $H = a_0 ^ \dagger a_1 ^ \dagger a_1 a_0-a_1 ^ \dagger a_0 ^ \dagger a_1 a_0 = 2a_0 ^ \dagger a_1 ^ \dagger a_1 a_0 $. Dit is een som van de bovenstaande voor waarden.</span><span class="sxs-lookup"><span data-stu-id="bb432-180">For instance, consider the Hamiltonian $H=a_0^\dagger a_1^\dagger a_1 a_0 - a_1^\dagger a_0^\dagger a_1 a_0 =2a_0^\dagger a_1^\dagger a_1 a_0$, which is a sum of terms constructed above.</span></span>
<span data-ttu-id="bb432-181">Het is niet altijd duidelijk voor de gebruiker dat deze gelijkwaardige voor waarden zijn, zodat ze afzonderlijk kunnen worden toegevoegd aan de Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="bb432-181">It may not always be clear to the user that these are equivalent terms, and so they may be added to the Hamiltonian separately.</span></span>
<span data-ttu-id="bb432-182">Het is ook mogelijk dat een van de bestaande voor waarden in de Hamiltonian wordt gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="bb432-182">Alternatively, one may be interested in modifying already-existing terms in the Hamiltonian.</span></span>
<span data-ttu-id="bb432-183">In deze gevallen kunnen we gelijkwaardige voor waarden als volgt combi neren.</span><span class="sxs-lookup"><span data-stu-id="bb432-183">In these cases, we may combine equivalent terms as follows.</span></span>
```csharp
    // We create a `FermionHamiltonian` instance to store the fermion terms.
    var hamiltonian = new FermionHamiltonian();

    // We now create two Hermitian fermion terms that are equivalent with respect to
    // anti-commutation and Hermitian symmetry.
    var terms = new[] {
        (new[] { 0, 1, 1, 0 }, 1.0),
        (new[] { 1, 0, 1, 0 }, 1.0) }
    .Select(o => (new HermitianFermionTerm(o.Item1.ToLadderSequence()), o.Item2.ToDoubleCoeff()));

    // Now add `terms` to the Hamiltonian.
    hamiltonian.AddRange(terms);

    // There is only one unique term. `nTerms == 1` is `true`.
    var nTerms = hamiltonian.CountTerms();
```
<span data-ttu-id="bb432-184">Door coefficienten van gelijkwaardige termen te combi neren, verlagen we het totale aantal voor waarden in de Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="bb432-184">By combining coefficients of equivalent terms, we reduce the total number of terms in the Hamiltonian.</span></span>
<span data-ttu-id="bb432-185">Later vermindert dit het aantal Quantum-Gates dat nodig is voor het simuleren van de Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="bb432-185">Later on, this reduces the number of quantum gates required to simulate the Hamiltonian.</span></span>

### <a name="internal-representation"></a><span data-ttu-id="bb432-186">Interne representatie</span><span class="sxs-lookup"><span data-stu-id="bb432-186">Internal Representation</span></span>

<span data-ttu-id="bb432-187">Een fermionic-Hamiltonian met interacties van één en twee hoofd tekst wordt weer gegeven in de tweede, getekende notatie als</span><span class="sxs-lookup"><span data-stu-id="bb432-187">A fermionic Hamiltonian with one- and two-body interactions is represented in second-quantized notation as</span></span>

<span data-ttu-id="bb432-188">$ $ \begin{align} H = \sum \_ {pq} H \_ {pq} a ^ \dagger \_ {p} a \_ {q} + \frac {1} {2} \sum \_ {pqrs} H \_ {pqrs} a ^ \dagger \_ {p} a ^ \dagger \_ {q} a \_ {r} a \_ {s}.</span><span class="sxs-lookup"><span data-stu-id="bb432-188">$$ \begin{align} H=\sum\_{pq}h\_{pq}a^\dagger\_{p}a\_{q}+\frac{1}{2}\sum\_{pqrs}h\_{pqrs}a^\dagger\_{p}a^\dagger\_{q}a\_{r}a\_{s}.</span></span>
<span data-ttu-id="bb432-189">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="bb432-189">\end{align} $$</span></span>

<span data-ttu-id="bb432-190">In deze notatie zijn er Maxi maal $N ^ 2 + N ^ 4 $ coëfficiënten.</span><span class="sxs-lookup"><span data-stu-id="bb432-190">In this notation, there are at most $N^2+N^4$ coefficients.</span></span>
<span data-ttu-id="bb432-191">Veel van deze coëfficiënten kunnen echter worden verzameld, aangezien ze overeenkomen met dezelfde operator.</span><span class="sxs-lookup"><span data-stu-id="bb432-191">However, many of these coefficients may be collected as they correspond to the same operator.</span></span>
<span data-ttu-id="bb432-192">Bijvoorbeeld als $p, q, r, s $ zijn afzonderlijke indices. we kunnen de anti-werk regels gebruiken om aan te tonen dat: $ $ a ^ \dagger \_ {p} a ^ \dagger \_ {q} a \_ {r} a \_ {s} =-a ^ \dagger \_ {q} a ^ \dagger \_ {p} a \_ {r} a \_ {s} =-a ^ \dagger \_ {p} a ^ \dagger \_ {q} a {s} a { \_ \_ r} = a ^ \dagger \_ {q} a ^ \dagger \_ {p} a {s} a \_ \_ {r}.</span><span class="sxs-lookup"><span data-stu-id="bb432-192">For instance, in the case where $p,q,r,s$ are distinct indices, we may use the anti-commutation rules to show that: $$ a^\dagger\_{p}a^\dagger\_{q}a\_{r}a\_{s} = -a^\dagger\_{q}a^\dagger\_{p}a\_{r}a\_{s} = -a^\dagger\_{p}a^\dagger\_{q}a\_{s}a\_{r} = a^\dagger\_{q}a^\dagger\_{p}a\_{s}a\_{r}.</span></span>
$$

<span data-ttu-id="bb432-193">Daarnaast heeft $H $ Hermitian, elke niet-Hermitian fermionic-operator, $h \_ {pqrs} a ^ \dagger \_ {p} a ^ \dagger \_ {q} a \_ {r} a \_ {s} $, een Hermitian geconjugeerde die zich ook bevindt in $H $.</span><span class="sxs-lookup"><span data-stu-id="bb432-193">Furthermore, as $H$ is Hermitian, every non-Hermitian fermionic operator, say $h\_{pqrs}a^\dagger\_{p}a^\dagger\_{q}a\_{r}a\_{s}$, has a Hermitian conjugate that is also found in $H$.</span></span> <span data-ttu-id="bb432-194">Om unieke groepen termen te indexeren die door deze Symmetries worden gekenmerkt, we definiëren een canonieke volg orde op de indices $ (i \_ 1, \cdots, i \_ n, j \_ 1, \cdots, j \_ m) $ van een reeks $n + m $ fermionic Opera tors $a ^ \dagger \_ {i \_ 1} \cdots a ^ \dagger \_ {i \_ n} een \_ {j m} \_ \_ \_ $as volgt:</span><span class="sxs-lookup"><span data-stu-id="bb432-194">In order to uniquely index groups of terms characterized by these symmetries, we define a canonical ordering on the indices $(i\_1,\cdots,i\_n,j\_1,\cdots,j\_m)$ of any sequence of $n+m$ fermionic operators $a^\dagger\_{i\_1}\cdots a^\dagger\_{i\_n}a\_{j\_1}\cdots a\_{j\_m}$as follows:</span></span>
-   <span data-ttu-id="bb432-195">Alle aanmaak operatoren $a ^ \dagger \_ {i \_ \cdot} $ worden geplaatst voordat alle Annihilation-opera tors $a \_ {j \_ \cdot} $.</span><span class="sxs-lookup"><span data-stu-id="bb432-195">All creation operators $a^\dagger\_{i\_\cdot}$ are placed before all annihilation operators $a\_{j\_\cdot}$.</span></span>
-   <span data-ttu-id="bb432-196">Alle indexen voor het maken van Opera tors worden in oplopende volg orde gesorteerd, die $i \_ 1< i \_ 2< \cdots < i \_ n $.</span><span class="sxs-lookup"><span data-stu-id="bb432-196">All creation operator indices are sorted in ascending order, that is $i\_1< i\_2< \cdots < i\_n$.</span></span>
-   <span data-ttu-id="bb432-197">Alle Annihilation-operator indexen zijn in aflopende volg orde gesorteerd, die $j \_ 1> j \_ 2 \cdots > j \_ m $.</span><span class="sxs-lookup"><span data-stu-id="bb432-197">All annihilation operator indices are sorted in descending order, that is $j\_1> j\_2 \cdots > j\_m$.</span></span>
-   <span data-ttu-id="bb432-198">De meest linkse index is kleiner dan of gelijk aan de meest rechtse index, die $i \_ 1 \ Le j \_ m $ is.</span><span class="sxs-lookup"><span data-stu-id="bb432-198">The left-most index is less than or equal to the right-most index, that is $i\_1\le j\_m$.</span></span>

<span data-ttu-id="bb432-199">Laat ons deze reeks canonieke bestelde indexen identificeren als $ $ \begin{align} (i \_ 1, \cdots, i n, \_ j \_ 1, \cdots, j \_ m) \in S \_ {n, m}.</span><span class="sxs-lookup"><span data-stu-id="bb432-199">Let us identify this set of canonically ordered indices as $$ \begin{align} (i\_1,\cdots,i\_n,j\_1,\cdots,j\_m) \in S\_{n,m}.</span></span>
<span data-ttu-id="bb432-200">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="bb432-200">\end{align} $$</span></span>

<span data-ttu-id="bb432-201">Met deze canonieke ordening kan de fermionic-Hamiltonian worden uitgedrukt als $ $ \begin{align} H = \sum \_ {(p, q) \In S \_ {1,1} } H ' \_ {pq} \frac{a ^ \dagger \_ {p} a \_ {q} + a ^ \dagger \_ {q} a \_ {p}} {2} + \sum \_ {(p, q, r, s) \in s \_ {2,2} } H ' \_ {pqrs} \frac{a ^ \dagger \_ {p} a ^ \dagger \_ {q} a \_ {r} a \_ {s} + a ^ \dagger \_ {s} a ^ \dagger \_ {r} a \_ {q} a \_ {p}} {2} , \end{align} $ $ met voldoende aangepaste integraals van één en twee elektroden $h \_ {pq} $ en $h \_ {pqrs} $.</span><span class="sxs-lookup"><span data-stu-id="bb432-201">With this canonical ordering, the fermionic Hamiltonian may be expressed as $$ \begin{align} H=\sum\_{(p,q)\in S\_{1,1}}h'\_{pq}\frac{a^\dagger\_{p}a\_{q}+a^\dagger\_{q}a\_{p}}{2}+\sum\_{(p,q,r,s)\in S\_{2,2}}h'\_{pqrs}\frac{a^\dagger\_{p}a^\dagger\_{q}a\_{r}a\_{s}+a^\dagger\_{s}a^\dagger\_{r}a\_{q}a\_{p}}{2}, \end{align} $$ with suitably adapted one- and two-electron integrals $h'\_{pq}$ and $h'\_{pqrs}$, respectively.</span></span>

