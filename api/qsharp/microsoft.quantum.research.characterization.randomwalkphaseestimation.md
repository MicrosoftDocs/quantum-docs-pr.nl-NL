---
uid: Microsoft.Quantum.Research.Characterization.RandomWalkPhaseEstimation
title: Bewerking RandomWalkPhaseEstimation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Characterization
qsharp.name: RandomWalkPhaseEstimation
qsharp.summary: Performs iterative phase estimation using a random walk to approximate Bayesian inference on the classical measurement results from a given oracle and eigenstate.
ms.openlocfilehash: 2c3afdd41da24a1f32f59f36f0f5c5ed29df1f0b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96226159"
---
# <a name="randomwalkphaseestimation-operation"></a><span data-ttu-id="f174b-102">Bewerking RandomWalkPhaseEstimation</span><span class="sxs-lookup"><span data-stu-id="f174b-102">RandomWalkPhaseEstimation operation</span></span>

<span data-ttu-id="f174b-103">Naam ruimte: [micro soft. Quantum. Research. karakte Rise](xref:Microsoft.Quantum.Research.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="f174b-103">Namespace: [Microsoft.Quantum.Research.Characterization](xref:Microsoft.Quantum.Research.Characterization)</span></span>

<span data-ttu-id="f174b-104">Pakket: [micro soft. Quantum. Research. karakte Rise](https://nuget.org/packages/Microsoft.Quantum.Research.Characterization) ring</span><span class="sxs-lookup"><span data-stu-id="f174b-104">Package: [Microsoft.Quantum.Research.Characterization](https://nuget.org/packages/Microsoft.Quantum.Research.Characterization)</span></span>


<span data-ttu-id="f174b-105">Voert een iteratieve fase schatting uit met behulp van een wille keurige Walk om Bayesiaanse te benaderen bij de klassieke meet resultaten van een bepaalde Oracle-en eigenstate.</span><span class="sxs-lookup"><span data-stu-id="f174b-105">Performs iterative phase estimation using a random walk to approximate Bayesian inference on the classical measurement results from a given oracle and eigenstate.</span></span>

```qsharp
operation RandomWalkPhaseEstimation (initialMean : Double, initialStdDev : Double, nMeasurements : Int, maxMeasurements : Int, unwind : Int, oracle : Microsoft.Quantum.Oracles.ContinuousOracle, targetState : Qubit[]) : Double
```


## <a name="input"></a><span data-ttu-id="f174b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f174b-106">Input</span></span>

### <a name="initialmean--double"></a><span data-ttu-id="f174b-107">initialMean: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f174b-107">initialMean : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f174b-108">Gemiddelde van de aanvankelijke voorafgaande distributie over $ \phi $.</span><span class="sxs-lookup"><span data-stu-id="f174b-108">Mean of the initial normal prior distribution over $\phi$.</span></span>


### <a name="initialstddev--double"></a><span data-ttu-id="f174b-109">initialStdDev: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f174b-109">initialStdDev : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f174b-110">Standaard afwijking van de aanvankelijke voorafgaande distributie over $ \phi $.</span><span class="sxs-lookup"><span data-stu-id="f174b-110">Standard deviation of the initial normal prior distribution over $\phi$.</span></span>


### <a name="nmeasurements--int"></a><span data-ttu-id="f174b-111">nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f174b-111">nMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f174b-112">Aantal metingen dat moet worden geaccepteerd in de uiteindelijke posterior-schatting.</span><span class="sxs-lookup"><span data-stu-id="f174b-112">Number of measurements to be accepted into the final posterior estimate.</span></span>


### <a name="maxmeasurements--int"></a><span data-ttu-id="f174b-113">maxMeasurements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f174b-113">maxMeasurements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f174b-114">Het totale aantal metingen dat kan worden uitgevoerd voordat de bewerking als mislukt wordt beschouwd.</span><span class="sxs-lookup"><span data-stu-id="f174b-114">Total number of measurements than can be taken before the operation is considered to have failed.</span></span>


### <a name="unwind--int"></a><span data-ttu-id="f174b-115">afwikkeling: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f174b-115">unwind : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f174b-116">Het aantal resultaten dat moet worden verg eten wanneer consistentie controles mislukt.</span><span class="sxs-lookup"><span data-stu-id="f174b-116">Number of results to forget when consistency checks fail.</span></span>


### <a name="oracle--continuousoracle"></a><span data-ttu-id="f174b-117">Oracle: [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span><span class="sxs-lookup"><span data-stu-id="f174b-117">oracle : [ContinuousOracle](xref:Microsoft.Quantum.Oracles.ContinuousOracle)</span></span>

<span data-ttu-id="f174b-118">Een bewerking die een unitary $U $ zodanig vertegenwoordigt dat $U (t) \ket{\phi} = e ^ {i t \phi}\ket{\phi} $ voor eigenstates $ \ket{\phi} $ met onbekende fase $ \phi \in \mathbb{R} ^ + $.</span><span class="sxs-lookup"><span data-stu-id="f174b-118">An operation representing a unitary $U$ such that $U(t)\ket{\phi} = e^{i t \phi}\ket{\phi}$ for eigenstates $\ket{\phi}$ with unknown phase $\phi \in \mathbb{R}^+$.</span></span>


### <a name="targetstate--qubit"></a><span data-ttu-id="f174b-119">targetState: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="f174b-119">targetState : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="f174b-120">Een REGI ster waarop $ wordt $U.</span><span class="sxs-lookup"><span data-stu-id="f174b-120">A register that $U$ acts on.</span></span>



## <a name="output--double"></a><span data-ttu-id="f174b-121">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f174b-121">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f174b-122">De laatste schatting $ \hat{\phi} \mathrel{: =} \expect [\phi] $, waarbij de verwachting groter is dan het posterior gegeven alle geaccepteerde gegevens.</span><span class="sxs-lookup"><span data-stu-id="f174b-122">The final estimate $\hat{\phi} \mathrel{:=} \expect[\phi]$ , where the expectation is over the posterior given all accepted data.</span></span>

## <a name="remarks"></a><span data-ttu-id="f174b-123">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="f174b-123">Remarks</span></span>

### <a name="iterative-phase-estimation-and-eigenstates"></a><span data-ttu-id="f174b-124">Schatting van iteratieve fase en Eigenstates</span><span class="sxs-lookup"><span data-stu-id="f174b-124">Iterative Phase Estimation and Eigenstates</span></span>

<span data-ttu-id="f174b-125">Over het algemeen hoeft het invoer register `eigenstate` geen eigenstate $ \ket{\phi} $ van $U $ te zijn, maar dit kan een superpositie zijn dan eigenstates.</span><span class="sxs-lookup"><span data-stu-id="f174b-125">In general, the input register `eigenstate` need not be an eigenstate $\ket{\phi}$ of $U$, but can be a superposition over eigenstates.</span></span> <span data-ttu-id="f174b-126">Stel dat de invoer status wordt gegeven door \begin{align} \ket{\psi} & = \sum \_ {j} \alpha \_ j \ket{\phi \_ j}, \end{align} waarbij $ \{ \alpha \_ j \} $ complexe coëfficiënten is, zoals $ \sum \_ j | \alpha \_ j | ^ 2 = $1 en waarbij $U \ket{\phi \_ j} = \phi \_ j\ket {\ Phi \_ j} $.</span><span class="sxs-lookup"><span data-stu-id="f174b-126">Suppose that the input state is given by \begin{align} \ket{\psi} & = \sum\_{j} \alpha\_j \ket{\phi\_j}, \end{align} where $\{\alpha\_j\}$ are complex coefficients such that $\sum\_j |\alpha\_j|^2 = 1$ and where $U\ket{\phi\_j} = \phi\_j\ket{\phi\_j}$.</span></span>

<span data-ttu-id="f174b-127">Vervolgens wordt de schatting van de iteratieve fase geconvergeerd naar één eigenstate, zoals beschreven in de [ontwikkel handleiding](xref:microsoft.quantum.libraries.characterization#iterative-phase-estimation-without-eigenstates).</span><span class="sxs-lookup"><span data-stu-id="f174b-127">Then, performing iterative phase estimation will eventually converge to a single eigenstate, as described in the [development guide](xref:microsoft.quantum.libraries.characterization#iterative-phase-estimation-without-eigenstates).</span></span>

### <a name="experiment-design"></a><span data-ttu-id="f174b-128">Experiment ontwerpen</span><span class="sxs-lookup"><span data-stu-id="f174b-128">Experiment Design</span></span>

<span data-ttu-id="f174b-129">De meet tijden $t $ en de inversie-hoeken $ \theta $ die zijn door gegeven aan `oracle` worden gekozen op basis van de *heuristiek* van de partikel, \Begin{align} \theta \sim \Pr (\phi), \quad t \approx \frac {1} {\variance{\phi}}.</span><span class="sxs-lookup"><span data-stu-id="f174b-129">The measurement times $t$ and inversion angles $\theta$ passed to `oracle` are chosen according to the *particle guess heuristic*, \begin{align} \theta \sim \Pr(\phi),\quad t \approx \frac{1}{\variance{\phi}}.</span></span>
<span data-ttu-id="f174b-130">\end{align} deze heuristiek is optimaal voor het verminderen van de verwachte posterior afwijking in een iteratieve fase schatting, onder de veronderstelling van een normaal voor gaande.</span><span class="sxs-lookup"><span data-stu-id="f174b-130">\end{align} This heuristic is optimal for reducing the expected posterior variance in iterative phase estimation under the assumption of a normal prior.</span></span>

### <a name="optimality"></a><span data-ttu-id="f174b-131">Optimale prestaties</span><span class="sxs-lookup"><span data-stu-id="f174b-131">Optimality</span></span>

<span data-ttu-id="f174b-132">Met deze bewerking wordt gebruikgemaakt van de optimale Estimator voor de fase $ \phi $, zoals geëvalueerd met behulp van het kwadratische verlies $L (\phi, \hat{\phi}) \mathrel{: =} (\phi-\hat{\phi}) ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="f174b-132">This operation approximates the optimal estimator for the phase $\phi$, as evaluated using the quadratic loss $L(\phi, \hat{\phi}) \mathrel{:=} (\phi - \hat{\phi})^2$.</span></span>

<span data-ttu-id="f174b-133">Zie de schatting van de [Bayesiaanse-fase](xref:microsoft.quantum.libraries.characterization#bayesian-phase-estimation) voor meer informatie over de statistieken van iteratieve fase schatting.</span><span class="sxs-lookup"><span data-stu-id="f174b-133">See [Bayesian Phase Estimation](xref:microsoft.quantum.libraries.characterization#bayesian-phase-estimation) for more details on the statistics of iterative phase estimation.</span></span>

## <a name="references"></a><span data-ttu-id="f174b-134">Referenties</span><span class="sxs-lookup"><span data-stu-id="f174b-134">References</span></span>

- <span data-ttu-id="f174b-135">Ferrie *et al.* 2011 [DOI: 10/TFX](https://doi.org/10.1007/s11128-012-0407-6), [arXiv: 1110.3067](https://arxiv.org/abs/1110.3067).</span><span class="sxs-lookup"><span data-stu-id="f174b-135">Ferrie *et al.* 2011 [doi:10/tfx](https://doi.org/10.1007/s11128-012-0407-6), [arXiv:1110.3067](https://arxiv.org/abs/1110.3067).</span></span>
- <span data-ttu-id="f174b-136">Wiebe *et al.* 2013 [DOI: 10/TF3](https://doi.org/10.1103/PhysRevLett.112.190501), [arXiv: 1309.0876](https://arxiv.org/abs/1309.0876)</span><span class="sxs-lookup"><span data-stu-id="f174b-136">Wiebe *et al.* 2013 [doi:10/tf3](https://doi.org/10.1103/PhysRevLett.112.190501), [arXiv:1309.0876](https://arxiv.org/abs/1309.0876)</span></span>
- <span data-ttu-id="f174b-137">Wiebe en Granade 2018 *(in voor bereiding)*.</span><span class="sxs-lookup"><span data-stu-id="f174b-137">Wiebe and Granade 2018 *(in preparation)*.</span></span>