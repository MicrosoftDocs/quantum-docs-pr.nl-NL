---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromPartialReflections
title: De functie AmplitudeAmplificationFromPartialReflections
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromPartialReflections
qsharp.summary: Amplitude amplification by partial reflections.
ms.openlocfilehash: 8fa6db7d5616f8c561191e3da00a69b05041b279
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191683"
---
# <a name="amplitudeamplificationfrompartialreflections-function"></a><span data-ttu-id="8b415-102">De functie AmplitudeAmplificationFromPartialReflections</span><span class="sxs-lookup"><span data-stu-id="8b415-102">AmplitudeAmplificationFromPartialReflections function</span></span>

<span data-ttu-id="8b415-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="8b415-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="8b415-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8b415-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8b415-105">Amplitude versterking door gedeeltelijke reflecties.</span><span class="sxs-lookup"><span data-stu-id="8b415-105">Amplitude amplification by partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromPartialReflections (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="8b415-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="8b415-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="8b415-107">fasen: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="8b415-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="8b415-108">Fasen van gedeeltelijke reflecties</span><span class="sxs-lookup"><span data-stu-id="8b415-108">Phases of partial reflections</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="8b415-109">startStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="8b415-109">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="8b415-110">Reflectie operator over begin status</span><span class="sxs-lookup"><span data-stu-id="8b415-110">Reflection operator about start state</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="8b415-111">targetStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="8b415-111">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="8b415-112">Reflectie operator over doel status</span><span class="sxs-lookup"><span data-stu-id="8b415-112">Reflection operator about target state</span></span>



## <a name="output--qubit--unit--is-adj--ctl"></a><span data-ttu-id="8b415-113">Output: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="8b415-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="8b415-114">Een bewerking waarbij amplitude versterking door gedeeltelijke reflecties wordt geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="8b415-114">An operation that implements amplitude amplification by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b415-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="8b415-115">Remarks</span></span>

<span data-ttu-id="8b415-116">Amplitude versterking is een speciaal geval van een obliviouse amplitude versterking waarbij er geen systeem qubits is en de Oblivious Oracle is ingesteld op identiteit.</span><span class="sxs-lookup"><span data-stu-id="8b415-116">Amplitude amplification is a special case of oblivious amplitude amplification where there are no system qubits and the oblivious oracle is set to identity.</span></span>
<span data-ttu-id="8b415-117">In de meeste gevallen `startQubits` wordt geïnitialiseerd in de status $ \ket{\text{start}} \_ $1, de $-$1-eigenstate van `startStateReflection` .</span><span class="sxs-lookup"><span data-stu-id="8b415-117">In most cases, `startQubits` is initialized in the state $\ket{\text{start}}\_1$, which is the $-1$ eigenstate of `startStateReflection`.</span></span>