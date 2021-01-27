---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromStatePreparation
title: De functie AmplitudeAmplificationFromStatePreparation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromStatePreparation
qsharp.summary: Amplitude amplification by oracles for partial reflections.
ms.openlocfilehash: e64ad5ad4e975483f20f92c0b070dd6788ef296b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847444"
---
# <a name="amplitudeamplificationfromstatepreparation-function"></a><span data-ttu-id="eb1fe-102">De functie AmplitudeAmplificationFromStatePreparation</span><span class="sxs-lookup"><span data-stu-id="eb1fe-102">AmplitudeAmplificationFromStatePreparation function</span></span>

<span data-ttu-id="eb1fe-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="eb1fe-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="eb1fe-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="eb1fe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="eb1fe-105">Een amplitude versterking van Oracle voor gedeeltelijke reflecties.</span><span class="sxs-lookup"><span data-stu-id="eb1fe-105">Amplitude amplification by oracles for partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromStatePreparation (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, stateOracle : Microsoft.Quantum.Oracles.StateOracle, idxFlagQubit : Int) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="eb1fe-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="eb1fe-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="eb1fe-107">fasen: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="eb1fe-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="eb1fe-108">Fasen van gedeeltelijke reflecties</span><span class="sxs-lookup"><span data-stu-id="eb1fe-108">Phases of partial reflections</span></span>


### <a name="stateoracle--stateoracle"></a><span data-ttu-id="eb1fe-109">stateOracle: [stateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span><span class="sxs-lookup"><span data-stu-id="eb1fe-109">stateOracle : [StateOracle](xref:Microsoft.Quantum.Oracles.StateOracle)</span></span>

<span data-ttu-id="eb1fe-110">Unitary Oracle $A $ waarmee begin status wordt voor bereid</span><span class="sxs-lookup"><span data-stu-id="eb1fe-110">Unitary oracle $A$ that prepares start state</span></span>


### <a name="idxflagqubit--int"></a><span data-ttu-id="eb1fe-111">idxFlagQubit: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eb1fe-111">idxFlagQubit : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eb1fe-112">Index om Qubit te markeren</span><span class="sxs-lookup"><span data-stu-id="eb1fe-112">Index to flag qubit</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="eb1fe-113">Output: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="eb1fe-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="eb1fe-114">Een bewerking waarbij amplitude versterking wordt geïmplementeerd door Oracle die worden geïmplementeerd door gedeeltelijke reflecties.</span><span class="sxs-lookup"><span data-stu-id="eb1fe-114">An operation that implements amplitude amplification by oracles that are implemented by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb1fe-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="eb1fe-115">Remarks</span></span>

<span data-ttu-id="eb1fe-116">Dit legt strengere voor waarden vast in de vorm van de begin-en doel status dan in `AmpAmpByReflectionPhases` .</span><span class="sxs-lookup"><span data-stu-id="eb1fe-116">This imposes stricter conditions on form of the start and target states than in `AmpAmpByReflectionPhases`.</span></span>
<span data-ttu-id="eb1fe-117">Er wordt van uitgegaan dat de doel status is gemarkeerd met $ \ket {1} \_ f $.</span><span class="sxs-lookup"><span data-stu-id="eb1fe-117">It is assumed that the target state is marked by $\ket{1}\_f$.</span></span>
<span data-ttu-id="eb1fe-118">Er wordt van uitgegaan dat \begin{align} A\ket {0} \_ {f} \ket {0} \_ s = \lambda\ket {1} \_ f\ket {\ text {target}} \_ s + \sqrt{1-| \lambda | ^ 2} \ket {0} \_ f\cdots, \end{align} in de meeste gevallen `flagQubit` en `auxiliaryRegister` worden geïnitialiseerd met de status $ \ket {0} \_ {f} \ket {0} \_ s $.</span><span class="sxs-lookup"><span data-stu-id="eb1fe-118">It is assumed that \begin{align} A\ket{0}\_{f}\ket{0}\_s= \lambda\ket{1}\_f\ket{\text{target}}\_s + \sqrt{1-|\lambda|^2}\ket{0}\_f\cdots, \end{align} In most cases, `flagQubit` and `auxiliaryRegister` are initialized in the state $\ket{0}\_{f}\ket{0}\_s$.</span></span>