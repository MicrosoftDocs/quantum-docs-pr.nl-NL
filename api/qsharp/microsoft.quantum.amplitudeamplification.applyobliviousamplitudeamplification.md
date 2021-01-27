---
uid: Microsoft.Quantum.AmplitudeAmplification.ApplyObliviousAmplitudeAmplification
title: Bewerking ApplyObliviousAmplitudeAmplification
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ApplyObliviousAmplitudeAmplification
qsharp.summary: Oblivious amplitude amplification by specifying partial reflections.
ms.openlocfilehash: c171021272076cc3960307523e25c4493bb49c5a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845860"
---
# <a name="applyobliviousamplitudeamplification-operation"></a><span data-ttu-id="b2e2a-102">Bewerking ApplyObliviousAmplitudeAmplification</span><span class="sxs-lookup"><span data-stu-id="b2e2a-102">ApplyObliviousAmplitudeAmplification operation</span></span>

<span data-ttu-id="b2e2a-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="b2e2a-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="b2e2a-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b2e2a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b2e2a-105">Oblivious-amplitude versterking door gedeeltelijke reflecties op te geven.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-105">Oblivious amplitude amplification by specifying partial reflections.</span></span>

```qsharp
operation ApplyObliviousAmplitudeAmplification (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, auxiliaryRegister : Qubit[], systemRegister : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="b2e2a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b2e2a-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="b2e2a-107">fasen: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="b2e2a-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="b2e2a-108">Fasen van gedeeltelijke reflecties</span><span class="sxs-lookup"><span data-stu-id="b2e2a-108">Phases of partial reflections</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="b2e2a-109">startStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="b2e2a-109">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="b2e2a-110">Reflectie operator over de begin status van de hulp registratie</span><span class="sxs-lookup"><span data-stu-id="b2e2a-110">Reflection operator about start state of auxiliary register</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="b2e2a-111">targetStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="b2e2a-111">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="b2e2a-112">Reflectie operator over de doel status van de hulp registratie</span><span class="sxs-lookup"><span data-stu-id="b2e2a-112">Reflection operator about target state of auxiliary register</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="b2e2a-113">signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="b2e2a-113">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="b2e2a-114">Unitary Oracle $O $ van `ObliviousOracle` het type dat gezamenlijk op de hulp-en systeem registers reageert.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-114">Unitary oracle $O$ of type `ObliviousOracle` that acts jointly on the auxiliary and system registers.</span></span>


### <a name="auxiliaryregister--qubit"></a><span data-ttu-id="b2e2a-115">auxiliaryRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b2e2a-115">auxiliaryRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b2e2a-116">Hulp registratie</span><span class="sxs-lookup"><span data-stu-id="b2e2a-116">Auxiliary register</span></span>


### <a name="systemregister--qubit"></a><span data-ttu-id="b2e2a-117">systemRegister: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="b2e2a-117">systemRegister : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="b2e2a-118">Systeem register</span><span class="sxs-lookup"><span data-stu-id="b2e2a-118">System register</span></span>



## <a name="output--unit"></a><span data-ttu-id="b2e2a-119">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b2e2a-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="b2e2a-120">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="b2e2a-120">Remarks</span></span>

<span data-ttu-id="b2e2a-121">Op basis van een bepaalde hulp begin status $ \ket{\Text{start}} \_ a $, een bepaalde hulp doel status $ \ket{\Text{target}} \_ a $ en een systeem status $ \ket{\psi} \_ s $, stel dat \begin{align} O\ket {\ text {start}} \_ a\ket {\ psi} \_ s = \lambda\ket{\Text{target}} \_ a U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket{\Text{target} ^ \perp} a\cdots \end{align} \_ voor sommige unitary $U $.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-121">Given a particular auxiliary start state $\ket{\text{start}}\_a$, a particular auxiliary target state $\ket{\text{target}}\_a$, and any system state $\ket{\psi}\_s$, suppose that \begin{align} O\ket{\text{start}}\_a\ket{\psi}\_s= \lambda\ket{\text{target}}\_a U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{\text{target}^\perp}\_a\cdots \end{align} for some unitary $U$.</span></span>
<span data-ttu-id="b2e2a-122">Met een opeenvolging van reflecties over de begin-en doel status van de hulp registratie die door toepassingen van `signalOracle` en haar adjoint wordt toegepast, kan de kans op voltooiing van het Toep assen van U worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-122">By a sequence of reflections about the start and target states on the auxiliary register interleaved by applications of `signalOracle` and its adjoint, the success probability of applying U may be altered.</span></span>

<span data-ttu-id="b2e2a-123">In de meeste gevallen `auxiliaryRegister` wordt geïnitialiseerd in de status $ \ket{\Text{start}} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-123">In most cases, `auxiliaryRegister` is initialized in the state $\ket{\text{start}}\_a$.</span></span>

## <a name="references"></a><span data-ttu-id="b2e2a-124">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="b2e2a-124">References</span></span>

<span data-ttu-id="b2e2a-125">Raadpleeg</span><span class="sxs-lookup"><span data-stu-id="b2e2a-125">See</span></span>

- <span data-ttu-id="b2e2a-126">[ *D.W. Berry, A.M. Childs, r. Cleve, R. Kothari, R.D. Somma*](https://arxiv.org/abs/1312.1414) voor de standaard versie.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-126">[ *D.W. Berry, A.M. Childs, R. Cleve, R. Kothari, R.D. Somma* ](https://arxiv.org/abs/1312.1414) for the standard version.</span></span>
  <span data-ttu-id="b2e2a-127">Raadpleeg</span><span class="sxs-lookup"><span data-stu-id="b2e2a-127">See</span></span>
- <span data-ttu-id="b2e2a-128">[ *G.H. laag, I.L. Chuang*](https://arxiv.org/abs/1610.06546) voor een generalisatie tot gedeeltelijke reflecties.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-128">[ *G.H. Low, I.L. Chuang* ](https://arxiv.org/abs/1610.06546) for a generalization to partial reflections.</span></span>