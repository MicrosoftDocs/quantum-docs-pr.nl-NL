---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardAmplitudeAmplification
title: De functie StandardAmplitudeAmplification
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardAmplitudeAmplification
qsharp.summary: Standard Amplitude Amplification algorithm
ms.openlocfilehash: 18228d45c4df280b004c595a7b0f1e2a607b8b2c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707686"
---
# <a name="standardamplitudeamplification-function"></a><span data-ttu-id="cd506-102">De functie StandardAmplitudeAmplification</span><span class="sxs-lookup"><span data-stu-id="cd506-102">StandardAmplitudeAmplification function</span></span>

<span data-ttu-id="cd506-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="cd506-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="cd506-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cd506-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cd506-105">Standaard amplitude versterking-algoritme</span><span class="sxs-lookup"><span data-stu-id="cd506-105">Standard Amplitude Amplification algorithm</span></span>

```qsharp
function StandardAmplitudeAmplification (nIterations : Int, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="cd506-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="cd506-106">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="cd506-107">nIterations: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cd506-107">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cd506-108">Aantal iteraties $n $ van amplitude versterking</span><span class="sxs-lookup"><span data-stu-id="cd506-108">Number of iterations $n$ of amplitude amplification</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="cd506-109">stateOracle: [stateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="cd506-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="cd506-110">Unitary Oracle $A $ waarmee begin status wordt voor bereid</span><span class="sxs-lookup"><span data-stu-id="cd506-110">Unitary oracle $A$ that prepares start state</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="cd506-111">idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cd506-111">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cd506-112">Index om Qubit te markeren</span><span class="sxs-lookup"><span data-stu-id="cd506-112">Index to flag qubit</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="cd506-113">Output: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="cd506-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="cd506-114">Een bewerking die de standaard amplitude-versterkte Quantum algoritme implementeert</span><span class="sxs-lookup"><span data-stu-id="cd506-114">An operation that implements the standard amplitude amplification quantum algorithm</span></span>

## <a name="remarks"></a><span data-ttu-id="cd506-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="cd506-115">Remarks</span></span>

<span data-ttu-id="cd506-116">Dit is het standaard algoritme voor amplitude versterking dat wordt verkregen door de keuze van de reflectie fasen die worden berekend door de vraag `AmpAmpPhasesStandard` dat \Begin{align} A\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ text {target}} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, \End{align} deze bewerking wordt voor bereid op de status \begin{align} \operatorname{AmpAmpByOracle}\ket {0} \_ {f} \ket {0} \_ s = \sin ((2n + 1) \sin ^ {-1} (\lambda)) \ket {1} \_ f\ket {\ text {target}} \_ s + \cdots\ket {0} \_ f \end{align} in de meeste gevallen `flagQubit` en `auxiliaryRegister` wordt geïnitialiseerd in de status $ \ket {0} \_ f\ket {0} \_ a $.</span><span class="sxs-lookup"><span data-stu-id="cd506-116">This is the standard amplitude amplification algorithm obtained by a choice of reflection phases computed by `AmpAmpPhasesStandard` Assuming that \begin{align} A\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\text{target}}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} this operation prepares the state \begin{align} \operatorname{AmpAmpByOracle}\ket{0}\_{f}\ket{0}\_s= \sin((2n+1)\sin^{-1}(\lambda))\ket{1}\_f\ket{\text{target}}\_s + \cdots\ket{0}\_f \end{align} In most cases, `flagQubit` and `auxiliaryRegister` is initialized in the state $\ket{0}\_f\ket{0}\_a$.</span></span>

## <a name="references"></a><span data-ttu-id="cd506-117">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="cd506-117">References</span></span>

- [<span data-ttu-id="cd506-118">*G. Brassard, P. Hoyer, M. Mosca, A. Tapp*</span><span class="sxs-lookup"><span data-stu-id="cd506-118"> *G. Brassard, P. Hoyer, M. Mosca, A. Tapp* </span></span>](https://arxiv.org/abs/quant-ph/0005055)