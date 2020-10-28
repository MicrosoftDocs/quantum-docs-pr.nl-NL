---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromStatePreparation
title: De functie AmplitudeAmplificationFromStatePreparation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromStatePreparation
qsharp.summary: Amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: 7725ff327e327578ff36242a2b1bc6d03fab0d0c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707770"
---
# <a name="amplitudeamplificationfromstatepreparation-function"></a><span data-ttu-id="77a25-102">De functie AmplitudeAmplificationFromStatePreparation</span><span class="sxs-lookup"><span data-stu-id="77a25-102">AmplitudeAmplificationFromStatePreparation function</span></span>

<span data-ttu-id="77a25-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="77a25-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="77a25-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="77a25-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="77a25-105">Een amplitude versterking van Oracle voor gedeeltelijke reflecties.</span><span class="sxs-lookup"><span data-stu-id="77a25-105">Amplitude amplification by oracles for partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="77a25-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="77a25-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="77a25-107">fasen: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="77a25-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="77a25-108">Fasen van gedeeltelijke reflecties</span><span class="sxs-lookup"><span data-stu-id="77a25-108">Phases of partial reflections</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="77a25-109">stateOracle: [stateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="77a25-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="77a25-110">Unitary Oracle $A $ waarmee begin status wordt voor bereid</span><span class="sxs-lookup"><span data-stu-id="77a25-110">Unitary oracle $A$ that prepares start state</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="77a25-111">idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="77a25-111">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="77a25-112">Index om Qubit te markeren</span><span class="sxs-lookup"><span data-stu-id="77a25-112">Index to flag qubit</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="77a25-113">Output: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="77a25-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="77a25-114">Een bewerking waarbij amplitude versterking wordt geïmplementeerd door Oracle die worden geïmplementeerd door gedeeltelijke reflecties.</span><span class="sxs-lookup"><span data-stu-id="77a25-114">An operation that implements amplitude amplification by oracles that are implemented by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="77a25-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="77a25-115">Remarks</span></span>

<span data-ttu-id="77a25-116">Dit legt strengere voor waarden vast in de vorm van de begin-en doel status dan in `AmpAmpByReflectionPhases` .</span><span class="sxs-lookup"><span data-stu-id="77a25-116">This imposes stricter conditions on form of the start and target states than in `AmpAmpByReflectionPhases`.</span></span>
<span data-ttu-id="77a25-117">Er wordt van uitgegaan dat de doel status is gemarkeerd met $ \ket {1} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="77a25-117">It is assumed that the target state is marked by $\ket{1}\_f$.</span></span>
<span data-ttu-id="77a25-118">Er wordt van uitgegaan dat \begin{align} A\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ text {target}} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, \end{align} in de meeste gevallen `flagQubit` en `auxiliaryRegister` worden geïnitialiseerd met de status $ \ket {0} \_ {f} \ket {0} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="77a25-118">It is assumed that \begin{align} A\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\text{target}}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} In most cases, `flagQubit` and `auxiliaryRegister` are initialized in the state $\ket{0}\_{f}\ket{0}\_s$.</span></span>