---
title: Hamiltonian Dynamics simuleren
description: Leer hoe u Trotter-Suzuki formules en qubitization kunt gebruiken om te werken met Hamiltonian-simulaties.
author: bradben
ms.author: v-benbra
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
uid: microsoft.quantum.chemistry.concepts.simulationalgorithms
no-loc:
- ':::no-loc(Q#):::'
- ':::no-loc($$v):::'
ms.openlocfilehash: a303d54476e42b98a14c6b452227b0e1346567c8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92691892"
---
# <a name="simulating-hamiltonian-dynamics"></a><span data-ttu-id="31340-103">Hamiltonian Dynamics simuleren</span><span class="sxs-lookup"><span data-stu-id="31340-103">Simulating Hamiltonian Dynamics</span></span>

<span data-ttu-id="31340-104">Zodra de Hamiltonian is uitgedrukt als som van elementaire Opera Tors, kan de dynamiek vervolgens worden gecompileerd in fundamentele poort bewerkingen met behulp van een host van bekende technieken.</span><span class="sxs-lookup"><span data-stu-id="31340-104">Once the Hamiltonian has been expressed as a sum of elementary operators the dynamics can then be compiled into fundamental gate operations using a host of well-known techniques.</span></span>
<span data-ttu-id="31340-105">Drie efficiënte benaderingen zijn Trotter: Suzuki formules, lineaire combi Naties van unitaries en qubitization.</span><span class="sxs-lookup"><span data-stu-id="31340-105">Three efficient approaches include are Trotter–Suzuki formulas, linear combinations of unitaries, and qubitization.</span></span>
<span data-ttu-id="31340-106">Deze drie benaderingen worden hieronder beschreven en geven concrete :::no-loc(Q#)::: voor beelden van hoe u deze methoden implementeert met behulp van de Hamiltonian-simulatie bibliotheek.</span><span class="sxs-lookup"><span data-stu-id="31340-106">We explain these three approaches below and give concrete :::no-loc(Q#)::: examples of how to implement these methods using the Hamiltonian simulation library.</span></span>


## <a name="trottersuzuki-formulas"></a><span data-ttu-id="31340-107">Trotter – Suzuki formules</span><span class="sxs-lookup"><span data-stu-id="31340-107">Trotter–Suzuki Formulas</span></span>
<span data-ttu-id="31340-108">Het idee achter Trotter – Suzuki formules is eenvoudig: de Hamiltonian als som van het eenvoudig simuleren van Hamiltonians en de totale evolutie te benaderen als een reeks van deze eenvoudigere evoluties.</span><span class="sxs-lookup"><span data-stu-id="31340-108">The idea behind Trotter–Suzuki formulas is simple: express the Hamiltonian as a sum of easy to simulate Hamiltonians and then approximate the total evolution as a sequence of these simpler evolutions.</span></span>
<span data-ttu-id="31340-109">U kunt met name $H = \ sum_ {j = 1} ^ m H_j $ de Hamiltonian zijn.</span><span class="sxs-lookup"><span data-stu-id="31340-109">In particular, let $H=\sum_{j=1}^m H_j$ be the Hamiltonian.</span></span>
<span data-ttu-id="31340-110">Then $ $ e ^ {-i \ sum_ {j = 1} ^ m H_j t} = \ prod_ {j = 1} ^ m e ^ {-iH_j t} + O (m ^ 2 t ^ 2), $ $. dat wil zeggen dat, als $t \ll $1, de fout in deze benadering verwaarloosbaar is.</span><span class="sxs-lookup"><span data-stu-id="31340-110">Then, $$ e^{-i\sum_{j=1}^m H_j t} =\prod_{j=1}^m e^{-iH_j t} + O(m^2 t^2), $$ which is to say that, if $t\ll 1$, then the error in this approximation becomes negligible.</span></span>
<span data-ttu-id="31340-111">Als $e ^ {-i H t} $ een normale exponentiële waarde was, zou de fout in deze benadering niet worden $O (m ^ 2 t ^ 2) $: de waarde is nul.</span><span class="sxs-lookup"><span data-stu-id="31340-111">Note that if $e^{-i H t}$ were an ordinary exponential then the error in this approximation would not be $O(m^2 t^2)$: it would be zero.</span></span>
<span data-ttu-id="31340-112">Deze fout treedt op omdat $e ^ {-iHt} $ een operator exponentiële is. als gevolg hiervan is er een fout opgetreden bij het gebruik van deze formule als gevolg van het feit dat de $H _j $-voor waarden niet werken ( *dat wil zeggen* $H _J H_k \ne H_k H_j $ in het algemeen).</span><span class="sxs-lookup"><span data-stu-id="31340-112">This error occurs because $e^{-iHt}$ is an operator exponential and as a result there is an error incurred when using this formula due to the fact that the $H_j$ terms do not commute ( *i.e.* , $H_j H_k \ne H_k H_j$ in general).</span></span>

<span data-ttu-id="31340-113">Als $t $ groot is, kunnen er nog steeds Trotter-Suzuki formules worden gebruikt om de dynamiek nauw keurig te simuleren door deze op te splitsen in een reeks korte fases.</span><span class="sxs-lookup"><span data-stu-id="31340-113">If $t$ is large, Trotter–Suzuki formulas can still be used to simulate the dynamics accurately by breaking it up into a sequence of short time-steps.</span></span>
<span data-ttu-id="31340-114">Laat $r $ het aantal stappen dat is uitgevoerd in de tijd evolutie, dus elke keer dat de stap wordt uitgevoerd voor tijd $t/r $.</span><span class="sxs-lookup"><span data-stu-id="31340-114">Let $r$ be the number of steps taken in the time evolution, so each time step runs for time $t/r$.</span></span> <span data-ttu-id="31340-115">Vervolgens hebben we dat $ $ e ^ {-i \ sum_ {j = 1} ^ m H_j t} = \left (\ prod_ {j = 1} ^ m e ^ {-iH_j t/r} \ right) ^ r + O (m ^ 2 t ^ 2/r), $ $ wat impliceert dat als $r $ wordt geschaald als $m ^ 2 t ^ 2/\ Epsilon $, de fout kan worden gemaakt Maxi maal $ \epsilon $ voor $ \epsilon>$0.</span><span class="sxs-lookup"><span data-stu-id="31340-115">Then, we have that $$ e^{-i\sum_{j=1}^m H_j t} =\left(\prod_{j=1}^m e^{-iH_j t/r}\right)^r + O(m^2 t^2/r), $$ which implies that if $r$ scales as $m^2 t^2/\epsilon$ then the error can be made at most $\epsilon$ for any $\epsilon>0$.</span></span>

<span data-ttu-id="31340-116">Nauw keurigere benaderingen kunnen worden gemaakt door een reeks operator exponentiëlen te maken, zodat de fout voorwaarden worden geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="31340-116">More accurate approximations can be built by constructing a sequence of operator exponentials such that the error terms cancel.</span></span>
<span data-ttu-id="31340-117">De eenvoudigste formule, de tweede volg orde Trotter-Suzuki formule, neemt de notatie $ $ U_2 (t) = \left (\ prod_ {j = 1} ^ {m} e ^ {-iH_j t/2R} \ prod_ {j = m} ^ 1 e ^ {-iH_j t/2R} \ right) ^ r = e ^ {-iHt} + O (m ^ 3 t ^ 3/r ^ 2), $ $ de fout die kan worden gemaakt van minder dan $ \epsilon $ voor $ \epsilon>$0 door het kiezen van $r $ te schalen als $m ^ {3/2} t ^ {3/2}/\sqrt {\ Epsilon} $.</span><span class="sxs-lookup"><span data-stu-id="31340-117">The simplest such formula, the second order Trotter-Suzuki formula, takes the form $$ U_2(t) = \left(\prod_{j=1}^{m} e^{-iH_j t/2r} \prod_{j=m}^1 e^{-iH_j t/2r}\right)^r = e^{-iHt} + O(m^3 t^3/r^2), $$ the error of which can be made less than $\epsilon$ for any $\epsilon>0$ by choosing $r$ to scale as $m^{3/2}t^{3/2}/\sqrt{\epsilon}$.</span></span>

<span data-ttu-id="31340-118">Zelfs hogere formules, met name ($ 2.000 $) volg orde voor $k>$0, kunnen recursief worden samengesteld: $ $ U_ {2.000} (t) = [U_ {t-2} (s_ka \~ )] ^ 2 U_ {t-2} ([1-4s_k] t) [U_ {2-2} (s_k \~ t)] ^ 2 = e ^ {-iHt} + O ((m t) ^ {2.000 + 1}/r ^ {2.000}), $ $ waar $s _k = (4-4 ^ {1/(2-1)}) ^ {-1} $.</span><span class="sxs-lookup"><span data-stu-id="31340-118">Even higher-order formulas, specifically ($2k$)th-order for $k>0$, can be constructed recursively: $$ U_{2k}(t) = [U_{2k-2}(s_k\~ t)]^2 U_{2k-2}([1-4s_k]t) [U_{2k-2}(s_k\~ t)]^2 = e^{-iHt} + O((m t)^{2k+1}/r^{2k}), $$ where $s_k = (4-4^{1/(2k-1)})^{-1}$.</span></span>

<span data-ttu-id="31340-119">Het eenvoudigste is de volgende vierde volg orde ($k = $2) formule, die oorspronkelijk is geïntroduceerd door Suzuki: $ $ U_4 (t) = [U_2 (s_2 \~ t)] ^ 2 U_2 ([1-4s_2] t) [U_2 (s_2 \~ t)] ^ 2 = e ^ {-iHt} + O (m ^ 5T ^ 5/r ^ 4), $ $ waar $s _2 = (4-4 ^ {1/3}) ^ {-1} $.</span><span class="sxs-lookup"><span data-stu-id="31340-119">The simplest is the following fourth order ($k=2$) formula, originally introduced by Suzuki: $$ U_4(t) = [U_2(s_2\~ t)]^2 U_2([1-4s_2]t) [U_2(s_2\~ t)]^2 = e^{-iHt} +O(m^5t^5/r^4), $$ where $s_2 = (4-4^{1/3})^{-1}$.</span></span>
<span data-ttu-id="31340-120">In het algemeen kunnen wille keurige formules met een hoge volg orde worden geconstrueerd. de kosten voor het gebruik van complexere integrators zijn echter vaak zwaarder dan de voor delen van de meeste praktische problemen.</span><span class="sxs-lookup"><span data-stu-id="31340-120">In general, arbitrarily high-order formulas can be similarly constructed; however, the costs incurred from using more complex integrators often outweigh the benefits beyond fourth order for most practical problems.</span></span>

<span data-ttu-id="31340-121">Om de bovenstaande strategieën te laten werken, moeten we een methode hebben voor het simuleren van een brede klasse van $e ^ {-iH_j t} $.</span><span class="sxs-lookup"><span data-stu-id="31340-121">In order to make the above strategies work, we need to have a method for simulating a wide class of $e^{-iH_j t}$.</span></span>
<span data-ttu-id="31340-122">De eenvoudigste familie van Hamiltonians en weliswaar het handigst, die we hier kunnen gebruiken, zijn Pauli Opera tors.</span><span class="sxs-lookup"><span data-stu-id="31340-122">The simplest family of Hamiltonians, and arguably most useful, that we could use here are Pauli operators.</span></span>
<span data-ttu-id="31340-123">Pauli-Opera tors kunnen gemakkelijk worden gesimuleerd, omdat ze kunnen worden gediagonaalt met behulp van Clifford-bewerkingen (die standaard Gates zijn in Quantum Computing).</span><span class="sxs-lookup"><span data-stu-id="31340-123">Pauli operators can be easily simulated because they can be diagonalized using Clifford operations (which are standard gates in quantum computing).</span></span>
<span data-ttu-id="31340-124">Nadat de eigenvalues zijn gediagonaalt, kunnen ze worden gevonden door de pariteit van de qubits waarop ze handelen te berekenen.</span><span class="sxs-lookup"><span data-stu-id="31340-124">Further, once they have been diagonalized, their eigenvalues can be found by computing the parity of the qubits on which they act.</span></span>

<span data-ttu-id="31340-125">Bijvoorbeeld: $ $ e ^ {-iX\otimes X t} = (H\otimes H) e ^ {-iZ\otimes Z t} (H\otimes H), $ $ waarbij $ $ e ^ {-i Z \otimes Z t} = \begin{bmatrix} e ^ {-it} & 0 & 0 & 0 </span><span class="sxs-lookup"><span data-stu-id="31340-125">For example, $$ e^{-iX\otimes X t}= (H\otimes H)e^{-iZ\otimes Z t}(H\otimes H), $$ where $$ e^{-i Z \otimes Z t} = \begin{bmatrix} e^{-it} & 0  & 0  & 0 </span></span>\\\
        <span data-ttu-id="31340-126">0 & e ^ {i t} & 0 & 0 </span><span class="sxs-lookup"><span data-stu-id="31340-126">0 & e^{i t}  & 0 & 0 </span></span>\\\
        <span data-ttu-id="31340-127">0 & 0 & e ^ {it} & 0 </span><span class="sxs-lookup"><span data-stu-id="31340-127">0 & 0 & e^{it} & 0 </span></span>\\\
        <span data-ttu-id="31340-128">0 & 0 & 0 & e ^ {-it} \end{bmatrix}.</span><span class="sxs-lookup"><span data-stu-id="31340-128">0 & 0 & 0 & e^{-it} \end{bmatrix}.</span></span>
<span data-ttu-id="31340-129">$ $ Hier $e ^ {-iHt} \ket {00} = e ^ {it} \ket {00} $ en $e ^ {-iHt} \ket {01} = e ^ {-it} \ket {01} $, die rechtstreeks kan worden gezien als gevolg van het feit dat de pariteit van $0 $ $0 $ is, terwijl de pariteit van de bit teken reeks $1 $ $1 $ is.</span><span class="sxs-lookup"><span data-stu-id="31340-129">$$ Here, $e^{-iHt} \ket{00} = e^{it} \ket{00}$ and $e^{-iHt} \ket{01} = e^{-it} \ket{01}$, which can be seen directly as a consequence of the fact that the parity of $00$ is $0$ while the parity of the bit string $01$ is $1$.</span></span>

<span data-ttu-id="31340-130">Exponentiële waarde van Pauli-Opera tors kunnen rechtstreeks worden geïmplementeerd in :::no-loc(Q#)::: met behulp van de <xref:Microsoft.Quantum.Intrinsic.Exp> bewerking:</span><span class="sxs-lookup"><span data-stu-id="31340-130">Exponentials of Pauli operators can be implemented directly in :::no-loc(Q#)::: using the <xref:Microsoft.Quantum.Intrinsic.Exp> operation:</span></span>
```qsharp
    using(qubits = Qubit[2]){
        let pauliString = [PauliX, PauliX];
        let evolutionTime = 1.0;

        // This applies 𝑒^{- 𝑖 𝑋⊗𝑋 𝑡} to qubits 0 and 1.
        Exp(pauliString, - evolutionTime, qubits);
    }
```

<span data-ttu-id="31340-131">Voor Fermionic Hamiltonians wijst de [Jordanië – Wigner](xref:microsoft.quantum.chemistry.concepts.jordanwigner) de Hamiltonian handig toe aan een som van Pauli-Opera tors.</span><span class="sxs-lookup"><span data-stu-id="31340-131">For Fermionic Hamiltonians, the [Jordan–Wigner decomposition](xref:microsoft.quantum.chemistry.concepts.jordanwigner) conveniently maps the Hamiltonian into a sum of Pauli operators.</span></span>
<span data-ttu-id="31340-132">Dit betekent dat de bovenstaande aanpak eenvoudig kan worden aangepast aan het simuleren van de schei kunde.</span><span class="sxs-lookup"><span data-stu-id="31340-132">This means that the above approach can easily be adapted to simulating chemistry.</span></span>
<span data-ttu-id="31340-133">In plaats van hand matig te herhalen over alle Pauli-voor waarden in de Jordan-Wigner vertegenwoordiging, hieronder vindt u een eenvoudig voor beeld van hoe een dergelijke simulatie binnen de schei kunde zou worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="31340-133">Rather than manually looping over all Pauli terms in the Jordan-Wigner representation, below is a simple example of how running such a simulation within the chemistry would look.</span></span>
<span data-ttu-id="31340-134">Ons begin punt is een [Jordanië – Wigner-code ring](xref:microsoft.quantum.chemistry.concepts.jordanwigner) van de Fermionic Hamiltonian, uitgedrukt in code als een exemplaar van de `JordanWignerEncoding` klasse.</span><span class="sxs-lookup"><span data-stu-id="31340-134">Our starting point is a [Jordan–Wigner encoding](xref:microsoft.quantum.chemistry.concepts.jordanwigner) of the Fermionic Hamiltonian, expressed in code as an instance of the `JordanWignerEncoding` class.</span></span>

```csharp
    // This example uses the following namespaces:
    // using Microsoft.Quantum.Chemistry.OrbitalIntegrals;
    // using Microsoft.Quantum.Chemistry.Fermion;
    // using Microsoft.Quantum.Chemistry.Pauli;
    // using Microsoft.Quantum.Chemistry.QSharpFormat;

    // We create an instance of the `FermionHamiltonian` objecclasst to store the terms.
    var hamiltonian = new OrbitalIntegralHamiltonian(new[] 
    {
        new OrbitalIntegral(new[] { 0, 1, 2, 3 }, 0.123),
        new OrbitalIntegral(new[] { 0, 1 }, 0.456)
    }).ToFermionHamiltonian(IndexConvention.UpDown);

    // We convert this fermion Hamiltonian to a Jordan-Wigner representation.
    var jordanWignerEncoding = hamiltonian.ToPauliHamiltonian(QubitEncoding.JordanWigner);

    // We now convert this representation into a format consumable by :::no-loc(Q#):::.
    var qSharpData = jordanWignerEncoding.ToQSharpFormat();
```

<span data-ttu-id="31340-135">Deze indeling van de Wigner-representatie die kan worden gebruikt door de :::no-loc(Q#)::: simulatie algoritmen is een door de gebruiker gedefinieerd type `JordanWignerEncodingData` .</span><span class="sxs-lookup"><span data-stu-id="31340-135">This format of the Jordan–Wigner representation that is consumable by the :::no-loc(Q#)::: simulation algorithms is a user-defined type `JordanWignerEncodingData`.</span></span>
<span data-ttu-id="31340-136">In :::no-loc(Q#)::: wordt deze indeling door gegeven aan een gebruiks vriendelijke functie `TrotterStepOracle` die een geschatte tijd van een operator retourneert met behulp van de Trotter-Suzuki integrator, naast de andere para meters die vereist zijn voor de uitvoering.</span><span class="sxs-lookup"><span data-stu-id="31340-136">Within :::no-loc(Q#):::, this format is passed to a convenience function `TrotterStepOracle` that returns an operator approximating time-evolution using the Trotter—Suzuki integrator, in addition to other parameters required for its run.</span></span>

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

// Let us now apply a single time-step.
using(qubits = Qubit[nQubits]){

    // Apply single step of time-evolution
    oracle(qubits);

    // Reset all qubits to the 0 state to be successfully released.
    ResetAll(qubits);
}
```

<span data-ttu-id="31340-137">Belang rijk: deze implementatie past een aantal optimalisaties toe die worden besproken in de [simulatie van de elektronische structuur Hamiltonians met behulp van quantum computers](https://arxiv.org/abs/1001.3855) en [verbeteren Quantum algoritmen voor quantum chemie](https://arxiv.org/abs/1403.1539) om het aantal vereiste draaiingen voor één Qubit te beperken, en om simulatie fouten te verminderen.</span><span class="sxs-lookup"><span data-stu-id="31340-137">Importantly, this implementation applies some optimizations discussed in [Simulation of Electronic Structure Hamiltonians Using Quantum Computers](https://arxiv.org/abs/1001.3855) and [Improving Quantum Algorithms for Quantum Chemistry](https://arxiv.org/abs/1403.1539) to minimize the number of single-qubit rotations required, as well as reduce simulation errors.</span></span>

## <a name="qubitization"></a><span data-ttu-id="31340-138">Qubitization</span><span class="sxs-lookup"><span data-stu-id="31340-138">Qubitization</span></span>

<span data-ttu-id="31340-139">Qubitization is een alternatieve aanpak voor simulatie waarbij ideeën van Quantum worden gebruikt om de Quantum dynamiek te simuleren.</span><span class="sxs-lookup"><span data-stu-id="31340-139">Qubitization is an alternative approach to simulation that uses ideas from quantum walks to simulate quantum dynamics.</span></span>
<span data-ttu-id="31340-140">Hoewel qubitization meer qubits dan Trotter formules vereist, biedt de methode een optimale schaal aanpassing met de ontwikkelings tijd en de fout tolerantie.</span><span class="sxs-lookup"><span data-stu-id="31340-140">While qubitization requires more qubits than Trotter formulas, the method promises optimal scaling with the evolution time and the error tolerance.</span></span>
<span data-ttu-id="31340-141">Daarom is het een aanbevolen methode geworden voor het simuleren van Hamiltonian Dynamics in het algemeen en voor het oplossen van het probleem met de elektronische structuur.</span><span class="sxs-lookup"><span data-stu-id="31340-141">For these reasons it has become a favored method for simulating Hamiltonian dynamics in general, and for solving the electronic structure problem in particular.</span></span>

<span data-ttu-id="31340-142">Op hoog niveau voert qubitization de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="31340-142">At a high level, qubitization accomplishes this through the following steps.</span></span>
<span data-ttu-id="31340-143">Laat eerst $H = \ sum_j h_j H_j $ voor unitary en Hermitian $H _J $ en $h _j \ge $0.</span><span class="sxs-lookup"><span data-stu-id="31340-143">First, let $H=\sum_j h_j H_j$ for unitary and Hermitian $H_j$ and $h_j\ge 0$.</span></span>
<span data-ttu-id="31340-144">Door een paar reflecties uit te voeren, implementeert qubitization een operator die gelijk is aan $ $W = e ^ {\pm i \cos ^ {-1} (h/| h | _1)}, $ $ waarbij $ | H | _1 = \ sum_j | h_j | $.</span><span class="sxs-lookup"><span data-stu-id="31340-144">By performing a pair of reflections, qubitization implements an operator that is equivalent to $$W=e^{\pm i \cos^{-1}(H/|h|_1)},$$ where $|h|_1 = \sum_j |h_j|$.</span></span>
<span data-ttu-id="31340-145">De volgende stap omvat het transformeren van de eigenvalues van de Walk-operator van $e ^ {i\pm \cos ^ {-1} (E_k/| h | _1)} $, waarbij $E _k $ de eigenvalues van $H $ is $e ^ {-iE_k t} $.</span><span class="sxs-lookup"><span data-stu-id="31340-145">The next step involves transforming the eigenvalues of the walk operator from $e^{i\pm \cos^{-1}(E_k/|h|_1)}$, where $E_k$ are the eigenvalues of $H$ to $e^{-iE_k t}$.</span></span>
<span data-ttu-id="31340-146">Dit kan worden bereikt met behulp van diverse Quantum-waarden transformatie methoden, waaronder [Quantum signaal verwerking](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.118.010501).</span><span class="sxs-lookup"><span data-stu-id="31340-146">This can be achieved using a variety of quantum singular value transformation methods including [quantum signal processing](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.118.010501).</span></span>

<span data-ttu-id="31340-147">Als er echter alleen statische hoeveel heden gewenst zijn (zoals de grond energie van de Hamiltonian), is het voldoende om de fase- [schatting](xref:microsoft.quantum.libraries.characterization) rechtstreeks toe te passen op $W $ om de grond energie van het resultaat te schatten door de cosinus van het resultaat te nemen.</span><span class="sxs-lookup"><span data-stu-id="31340-147">Alternatively, if only static quantities are desired (such as the ground state energy of the Hamiltonian) then it suffices to apply [phase estimation](xref:microsoft.quantum.libraries.characterization) directly to $W$ to estimate the ground state energy from the result by taking the cosine of the result.</span></span>
<span data-ttu-id="31340-148">Dit is belang rijk omdat de Spectral-trans formatie klassiek kan worden uitgevoerd in plaats van een Quantum waarde transformatie methode te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="31340-148">This is significant because it allows the spectral transformation to be performed classically rather than using a quantum singular value transformation method.</span></span>

<span data-ttu-id="31340-149">Op een meer gedetailleerd niveau vereist de implementatie van qubitization twee subroutines die de interfaces bieden voor de Hamiltonian.</span><span class="sxs-lookup"><span data-stu-id="31340-149">On a more detailed level, the implementation of qubitization requires two subroutines that provide the interfaces for the Hamiltonian.</span></span>
<span data-ttu-id="31340-150">In tegens telling tot Trotter-Suzuki-methoden zijn deze subroutines Quantum niet klassiek en is de implementatie nood zakelijk om logarithmically meer qubits te gebruiken dan nodig is voor een op Trotter gebaseerde simulatie.</span><span class="sxs-lookup"><span data-stu-id="31340-150">Unlike Trotter–Suzuki methods, these subroutines are quantum not classical and their implementation will necessitate using logarithmically more qubits than would be required for a Trotter-based simulation.</span></span>

<span data-ttu-id="31340-151">De eerste Quantum subroutine die qubitization gebruikt, heet $ \operatorname{Select} $ en is toegezegd om \begin{Equation} \operatorname{Select} \ket{j} \ket{\psi} = \ket{j} H_j \ket{\psi}, \end{Equation} te leveren waarbij elke $H _j $ wordt aangenomen dat het Hermitian en unitary is.</span><span class="sxs-lookup"><span data-stu-id="31340-151">The first quantum subroutine that qubitization uses is called $\operatorname{Select}$ and it is promised to yield \begin{equation} \operatorname{Select} \ket{j} \ket{\psi} = \ket{j} H_j \ket{\psi}, \end{equation} where each $H_j$ is assumed to be Hermitian and unitary.</span></span>
<span data-ttu-id="31340-152">Hoewel dit waarschijnlijk beperkend lijkt, herinnert u zich dat Pauli-Opera tors Hermitian en unitary zijn, en dat toepassingen zoals de simulatie van quantum chemie natuurlijk in dit kader vallen.</span><span class="sxs-lookup"><span data-stu-id="31340-152">While this may seem to be restrictive, recall that Pauli operators are Hermitian and unitary and so applications like quantum chemistry simulation naturally fall into this framework.</span></span>
<span data-ttu-id="31340-153">De $ \operatorname{Select} $-bewerking, mogelijk verrassend, is eigenlijk een reflectie bewerking.</span><span class="sxs-lookup"><span data-stu-id="31340-153">The $\operatorname{Select}$ operation, perhaps surprisingly, is actually a reflection operation.</span></span>
<span data-ttu-id="31340-154">Dit kan worden gezien uit het feit dat $ \operatorname{Select} ^ 2 \ Ket {j} \ket{\psi} = \ket{j} \ket{\psi} $ sinds elke $H _j $ unitary en Hermitian is en dus eigenvalues $ \pm $1.</span><span class="sxs-lookup"><span data-stu-id="31340-154">This can be seen from the fact that $\operatorname{Select}^2\ket{j} \ket{\psi} = \ket{j} \ket{\psi}$ since each $H_j$ is unitary and Hermitian and thus has eigenvalues $\pm 1$.</span></span>

<span data-ttu-id="31340-155">De tweede subroutine heet $ \operatorname{Prepare} $.</span><span class="sxs-lookup"><span data-stu-id="31340-155">The second subroutine is called $\operatorname{Prepare}$.</span></span>
<span data-ttu-id="31340-156">Terwijl de Select-bewerking een manier biedt om alle Hamiltonian-voor waarden te verkrijgen $H _j $ de subroutine voor bereiding de methode heeft om toegang te krijgen tot de coëfficiënten $h _j $, \begin{Equation} \operatorname{Prepare}\ket {0} = \ sum_j \sqrt{\frac{h_j} {| H | _1}} \ket{j}.</span><span class="sxs-lookup"><span data-stu-id="31340-156">While the select operation provides a means to coherently access each of the Hamiltonian terms $H_j$ the prepare subroutine gives a method for accessing the coefficients $h_j$, \begin{equation} \operatorname{Prepare}\ket{0} = \sum_j \sqrt{\frac{h_j}{|h|_1}}\ket{j}.</span></span>
<span data-ttu-id="31340-157">\end{Equation}, met behulp van een geteste gestuurde Phase-poort, zien we dat $ $ \Lambda\ket {0} ^ {\otimes n} = \begin{cases} \- \ket{x} & \Text{if} x = 0 </span><span class="sxs-lookup"><span data-stu-id="31340-157">\end{equation} Then, by using a multiply controlled phase gate, we see that $$ \Lambda\ket{0}^{\otimes n} = \begin{cases} \-\ket{x} & \text{if } x = 0 </span></span>\\\
        <span data-ttu-id="31340-158">\ket{x} & \Text{otherwise} \end{cases}.</span><span class="sxs-lookup"><span data-stu-id="31340-158">\ket{x}   & \text{otherwise} \end{cases}.</span></span>
$$

<span data-ttu-id="31340-159">De $ \operatorname{Prepare} $-bewerking wordt niet rechtstreeks in qubitization gebruikt, maar wordt gebruikt voor het implementeren van een reflectie over de status die $ \operatorname{Prepare} $ $ $ \begin{align} R &amp; = 1-2 \ operatornaam {Prepare} \ket {0} \bra \operatorname{Prepare} {0} ^ {-1} \\ \\ &amp; = \operatorname{Prepare} \Lambda \operatorname{Prepare} ^ {-1} .</span><span class="sxs-lookup"><span data-stu-id="31340-159">The $\operatorname{Prepare}$ operation is not used directly in qubitization, but rather is used to implement a reflection about the state that $\operatorname{Prepare}$ creates $$ \begin{align} R &amp; = 1 - 2\operatorname{Prepare} \ket{0}\bra{0} \operatorname{Prepare}^{-1} \\\\ &amp; = \operatorname{Prepare} \Lambda \operatorname{Prepare}^{-1}.</span></span>
<span data-ttu-id="31340-160">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="31340-160">\end{align} $$</span></span>

<span data-ttu-id="31340-161">De Walk-operator $W $ kan worden uitgedrukt in termen van $ \operatorname{Select} $ en $R $-bewerkingen als $ $ W = \operatorname{Select} R, $ $. Dit kan worden gezien als een operator die equivalent is (Maxi maal een isometry), kan worden geïmplementeerd om te $e ^ {\pm i \cos ^ {-1} (h/| h | _1)} $.</span><span class="sxs-lookup"><span data-stu-id="31340-161">The walk operator, $W$, can be expressed in terms of the $\operatorname{Select}$ and $R$ operations as $$ W = \operatorname{Select} R, $$ which again can be seen to implement an operator that is equivalent (up to an isometry) to $e^{\pm i \cos^{-1}(H/|h|_1)}$.</span></span>

<span data-ttu-id="31340-162">Deze subroutines zijn eenvoudig in te stellen in :::no-loc(Q#)::: .</span><span class="sxs-lookup"><span data-stu-id="31340-162">These subroutines are easy to set up in :::no-loc(Q#):::.</span></span>
<span data-ttu-id="31340-163">Denk bijvoorbeeld aan de eenvoudige Qubit-transversale Ising Hamiltonian waarbij $H = X_1 + X_2 + Z_1 Z_2 $.</span><span class="sxs-lookup"><span data-stu-id="31340-163">As an example, consider the simple qubit transverse-Ising Hamiltonian where $H = X_1 + X_2 + Z_1 Z_2$.</span></span>
<span data-ttu-id="31340-164">In dit geval :::no-loc(Q#)::: wordt de code waarmee de $ \operatorname{Select} $-bewerking zou worden geïmplementeerd, aangeroepen door <xref:Microsoft.Quantum.Canon.MultiplexOperations> , terwijl de $ \operatorname{Prepare} $-bewerking kan worden geïmplementeerd met <xref:Microsoft.Quantum.Preparation.PrepareArbitraryState> .</span><span class="sxs-lookup"><span data-stu-id="31340-164">In this case, :::no-loc(Q#)::: code that would implement the $\operatorname{Select}$ operation is invoked by <xref:Microsoft.Quantum.Canon.MultiplexOperations>, whereas the $\operatorname{Prepare}$ operation can be implemented using <xref:Microsoft.Quantum.Preparation.PrepareArbitraryState>.</span></span>
<span data-ttu-id="31340-165">Een voor beeld van het simuleren van het Hubbard model kan worden gevonden als een voor [ :::no-loc(Q#)::: beeld](https://github.com/microsoft/Quantum/tree/main/samples/simulation/hubbard).</span><span class="sxs-lookup"><span data-stu-id="31340-165">An example that involves simulating the Hubbard model can be found as a [:::no-loc(Q#)::: sample](https://github.com/microsoft/Quantum/tree/main/samples/simulation/hubbard).</span></span>

<span data-ttu-id="31340-166">Het hand matig opgeven van deze stappen voor wille keurige schei problemen zou veel moeite vergen, wat wordt voor komen met behulp van de Library chemie.</span><span class="sxs-lookup"><span data-stu-id="31340-166">Manually specifying these steps for arbitrary chemistry problems would require much effort, which is avoided using the chemistry library.</span></span>
<span data-ttu-id="31340-167">Op dezelfde manier als het simulatie algoritme Trotter-Suzuki wordt de `JordanWignerEncodingData` wordt door gegeven aan de functie voor gemak `QubitizationOracle` die de Walk-operator retourneert, naast de andere para meters die vereist zijn voor de uitvoering.</span><span class="sxs-lookup"><span data-stu-id="31340-167">Similarly to the Trotter–Suzuki simulation algorithm above, the `JordanWignerEncodingData` is passed to the convenience function `QubitizationOracle` that returns the walk-operator, in addition to other parameters required for its run.</span></span>

```qsharp
// qSharpData passed from driver
let qSharpData = ... 

// `oracle` is an operation that applies a single time-step of evolution for duration `stepSize`.
// `rescale` is just `1.0/oneNorm`, where oneNorm is the sum of absolute values of all probabilities in state prepared by `Prepare`.
// `nQubits` is the number of qubits that must be allocated to run the `oracle` operation.
let (nQubits, (rescale, oracle)) =  QubitizationOracle (qSharpData, stepSize, integratorOrder);

// Let us now apply a single step of the quantum walk.
using(qubits = Qubit[nQubits]){

    // Apply single step of quantum walk.
    oracle(qubits);

    // Reset all qubits to the 0 state to be successfully released.
    ResetAll(qubits);
}
```

<span data-ttu-id="31340-168">Belang rijk: de implementatie <xref:Microsoft.Quantum.Chemistry.JordanWigner.QubitizationOracle> is van toepassing op een wille keurige Hamiltonians die is opgegeven als een lineaire combi natie van Pauli-teken reeksen.</span><span class="sxs-lookup"><span data-stu-id="31340-168">Importantly, the implementation <xref:Microsoft.Quantum.Chemistry.JordanWigner.QubitizationOracle> is applicable to arbitrary Hamiltonians specified as a linear combination of Pauli strings.</span></span>
<span data-ttu-id="31340-169">Er wordt een versie die is geoptimaliseerd voor chemie simulaties aangeroepen met <xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedQubitizationOracle> .</span><span class="sxs-lookup"><span data-stu-id="31340-169">A version optimized for chemistry simulations is invoked using <xref:Microsoft.Quantum.Chemistry.JordanWigner.OptimizedQubitizationOracle>.</span></span>
<span data-ttu-id="31340-170">Deze versie is geoptimaliseerd om het aantal T-poorten te minimaliseren met behulp van technieken die worden beschreven in de [code ring van elektronische spectra in Quantum circuits met lineaire-T-complexiteit](https://arxiv.org/abs/1805.03662).</span><span class="sxs-lookup"><span data-stu-id="31340-170">This version is optimized to minimize the number of T gates using techniques discussed in [Encoding Electronic Spectra in Quantum Circuits with Linear T Complexity](https://arxiv.org/abs/1805.03662).</span></span>
