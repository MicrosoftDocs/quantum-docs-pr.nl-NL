---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardAmplitudeAmplification
title: De functie StandardAmplitudeAmplification
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardAmplitudeAmplification
qsharp.summary: Standard Amplitude Amplification algorithm
ms.openlocfilehash: 23a2b3dbe5ea404059994167f69e11458c0c22ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191173"
---
# <a name="standardamplitudeamplification-function"></a><span data-ttu-id="5c8f8-102">De functie StandardAmplitudeAmplification</span><span class="sxs-lookup"><span data-stu-id="5c8f8-102">StandardAmplitudeAmplification function</span></span>

<span data-ttu-id="5c8f8-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="5c8f8-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="5c8f8-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5c8f8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5c8f8-105">Standaard amplitude versterking-algoritme</span><span class="sxs-lookup"><span data-stu-id="5c8f8-105">Standard Amplitude Amplification algorithm</span></span>

```qsharp
function StandardAmplitudeAmplification (nIterations : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="5c8f8-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5c8f8-106">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="5c8f8-107">nIterations: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5c8f8-107">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5c8f8-108">Aantal iteraties $n $ van amplitude versterking</span><span class="sxs-lookup"><span data-stu-id="5c8f8-108">Number of iterations $n$ of amplitude amplification</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="5c8f8-109">stateOracle: [stateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="5c8f8-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="5c8f8-110">Unitary Oracle $A $ waarmee begin status wordt voor bereid</span><span class="sxs-lookup"><span data-stu-id="5c8f8-110">Unitary oracle $A$ that prepares start state</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="5c8f8-111">idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5c8f8-111">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5c8f8-112">Index om Qubit te markeren</span><span class="sxs-lookup"><span data-stu-id="5c8f8-112">Index to flag qubit</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="5c8f8-113">Output: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="5c8f8-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="5c8f8-114">Een bewerking die de standaard amplitude-versterkte Quantum algoritme implementeert</span><span class="sxs-lookup"><span data-stu-id="5c8f8-114">An operation that implements the standard amplitude amplification quantum algorithm</span></span>

## <a name="remarks"></a><span data-ttu-id="5c8f8-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="5c8f8-115">Remarks</span></span>

<span data-ttu-id="5c8f8-116">Dit is het standaard algoritme voor amplitude versterking dat wordt verkregen door de keuze van de reflectie fasen die worden berekend door de vraag `AmpAmpPhasesStandard` dat \Begin{align} A\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ text {target}} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, \End{align} deze bewerking wordt voor bereid op de status \begin{align} \operatorname{AmpAmpByOracle}\ket {0} \_ {f} \ket {0} \_ s = \sin ((2n + 1) \sin ^ {-1} (\lambda)) \ket {1} \_ f\ket {\ text {target}} \_ s + \cdots\ket {0} \_ f \end{align} in de meeste gevallen `flagQubit` en `auxiliaryRegister` wordt geïnitialiseerd in de status $ \ket {0} \_ f\ket {0} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="5c8f8-116">This is the standard amplitude amplification algorithm obtained by a choice of reflection phases computed by `AmpAmpPhasesStandard` Assuming that \begin{align} A\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\text{target}}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} this operation prepares the state \begin{align} \operatorname{AmpAmpByOracle}\ket{0}\_{f}\ket{0}\_s= \sin((2n+1)\sin^{-1}(\lambda))\ket{1}\_f\ket{\text{target}}\_s + \cdots\ket{0}\_f \end{align} In most cases, `flagQubit` and `auxiliaryRegister` is initialized in the state $\ket{0}\_f\ket{0}\_a$.</span></span>

## <a name="references"></a><span data-ttu-id="5c8f8-117">Referenties</span><span class="sxs-lookup"><span data-stu-id="5c8f8-117">References</span></span>

- [<span data-ttu-id="5c8f8-118">*G. Brassard, P. Hoyer, M. Mosca, A. Tapp*</span><span class="sxs-lookup"><span data-stu-id="5c8f8-118"> *G. Brassard, P. Hoyer, M. Mosca, A. Tapp* </span></span>](https://arxiv.org/abs/quant-ph/0005055)