---
uid: Microsoft.Quantum.AmplitudeAmplification.ObliviousAmplitudeAmplificationFromStatePreparation
title: De functie ObliviousAmplitudeAmplificationFromStatePreparation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: ObliviousAmplitudeAmplificationFromStatePreparation
qsharp.summary: Oblivious amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 9975d26af8f9beb2b91e409ad78159d6f04936e3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707722"
---
# <a name="obliviousamplitudeamplificationfromstatepreparation-function"></a><span data-ttu-id="4ebac-102">De functie ObliviousAmplitudeAmplificationFromStatePreparation</span><span class="sxs-lookup"><span data-stu-id="4ebac-102">ObliviousAmplitudeAmplificationFromStatePreparation function</span></span>

<span data-ttu-id="4ebac-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="4ebac-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="4ebac-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4ebac-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4ebac-105">Oblivious-amplitude versterking door Oracle voor gedeeltelijke reflecties.</span><span class="sxs-lookup"><span data-stu-id="4ebac-105">Oblivious amplitude amplification by oracles for partial reflections.</span></span>

```qsharp
function ObliviousAmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateOracle : Microsoft.Quantum.Oracles.DeterministicStateOracle, signalOracle : Microsoft.Quantum.Oracles.ObliviousOracle, idxFlagQubit : Int) : ((Qubit[], Qubit[]) => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="4ebac-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="4ebac-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="4ebac-107">fasen: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="4ebac-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="4ebac-108">Fasen van gedeeltelijke reflecties</span><span class="sxs-lookup"><span data-stu-id="4ebac-108">Phases of partial reflections</span></span>


### <a name="startstateoracle--deterministicstateoracle"></a><span data-ttu-id="4ebac-109">startStateOracle: [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span><span class="sxs-lookup"><span data-stu-id="4ebac-109">startStateOracle : [DeterministicStateOracle](xref:Microsoft.Quantum.Oracles.DeterministicStateOracle)</span></span>

<span data-ttu-id="4ebac-110">Unitary Oracle $A $ waarmee de start status van de hulp wordt voor bereid</span><span class="sxs-lookup"><span data-stu-id="4ebac-110">Unitary oracle $A$ that prepares auxiliary start state</span></span>


### <a name="signaloracle--obliviousoracle"></a><span data-ttu-id="4ebac-111">signalOracle: [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span><span class="sxs-lookup"><span data-stu-id="4ebac-111">signalOracle : [ObliviousOracle](xref:Microsoft.Quantum.Oracles.ObliviousOracle)</span></span>

<span data-ttu-id="4ebac-112">Unitary Oracle $O $ van `ObliviousOracle` het type dat gezamenlijk op de hulp-en systeem register reageert</span><span class="sxs-lookup"><span data-stu-id="4ebac-112">Unitary oracle $O$ of type `ObliviousOracle` that acts jointly on the auxiliary and system register</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="4ebac-113">idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4ebac-113">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4ebac-114">Index naar één Qubit-vlag registreren</span><span class="sxs-lookup"><span data-stu-id="4ebac-114">Index to single-qubit flag register</span></span>



## <a name="output--qubitqubit--unit-adj--ctl"></a><span data-ttu-id="4ebac-115">Output: ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="4ebac-115">Output : ([Qubit](xref:microsoft.quantum.lang-ref.qubit)[],[Qubit](xref:microsoft.quantum.lang-ref.qubit)[]) => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="4ebac-116">Een bewerking die Oblivious amplitude-versterking implementeert op basis van gedeeltelijke reflecties.</span><span class="sxs-lookup"><span data-stu-id="4ebac-116">An operation that implements oblivious amplitude amplification based on partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ebac-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="4ebac-117">Remarks</span></span>

<span data-ttu-id="4ebac-118">Dit legt strengere voor waarden vast in de vorm van het hulp start en de doel statussen dan in `AmpAmpObliviousByReflectionPhases` .</span><span class="sxs-lookup"><span data-stu-id="4ebac-118">This imposes stricter conditions on form of the auxiliary start and target states than in `AmpAmpObliviousByReflectionPhases`.</span></span>
<span data-ttu-id="4ebac-119">Er wordt van uitgegaan dat $A \ket {0} \_ f\ket {0} \_ A = \ket{\Text{start}} \_ {FA} $ de hulp start status $ \ket{\Text{start}} \_ {FA} $ voorbereidt op basis van de reken kracht $ \ket {0} \_ f\ket {0} $.</span><span class="sxs-lookup"><span data-stu-id="4ebac-119">It is assumed that $A\ket{0}\_f\ket{0}\_a= \ket{\text{start}}\_{fa}$ prepares the auxiliary start state $\ket{\text{start}}\_{fa}$ from the computational basis $\ket{0}\_f\ket{0}$.</span></span>
<span data-ttu-id="4ebac-120">Er wordt van uitgegaan dat de doel status is gemarkeerd met $ \ket {1} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="4ebac-120">It is assumed that the target state is marked by $\ket{1}\_f$.</span></span>
<span data-ttu-id="4ebac-121">Er wordt van uitgegaan dat \begin{align} O\ket {\ text {start}} \_ {FA} \ket{\psi} \_ s = \lambda\ket {1} \_ f\ket {\ text {overal}} \_ a\ket {\ text {target}} \_ s U \ket{\psi} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, \end{align} voor sommige unitary $U $.</span><span class="sxs-lookup"><span data-stu-id="4ebac-121">It is assumed that \begin{align} O\ket{\text{start}}\_{fa}\ket{\psi}\_s= \lambda\ket{1}\_f\ket{\text{anything}}\_a\ket{\text{target}}\_s U \ket{\psi}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} for some unitary $U$.</span></span>