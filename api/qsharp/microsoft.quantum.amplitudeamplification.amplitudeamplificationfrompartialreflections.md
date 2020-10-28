---
uid: Microsoft.Quantum.AmplitudeAmplification.AmplitudeAmplificationFromPartialReflections
title: De functie AmplitudeAmplificationFromPartialReflections
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: AmplitudeAmplificationFromPartialReflections
qsharp.summary: Amplitude amplification by partial reflections.
ms.openlocfilehash: fc7c2c0d05ea626f7f7e5d8ebf3ce5ecea61390b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707771"
---
# <a name="amplitudeamplificationfrompartialreflections-function"></a><span data-ttu-id="fae9f-102">De functie AmplitudeAmplificationFromPartialReflections</span><span class="sxs-lookup"><span data-stu-id="fae9f-102">AmplitudeAmplificationFromPartialReflections function</span></span>

<span data-ttu-id="fae9f-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="fae9f-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="fae9f-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fae9f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fae9f-105">Amplitude versterking door gedeeltelijke reflecties.</span><span class="sxs-lookup"><span data-stu-id="fae9f-105">Amplitude amplification by partial reflections.</span></span>

```qsharp
function AmplitudeAmplificationFromPartialReflections (phases : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases, startStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle, targetStateReflection : Microsoft.Quantum.Oracles.ReflectionOracle) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="fae9f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="fae9f-106">Input</span></span>

### <a name="phases--reflectionphases"></a><span data-ttu-id="fae9f-107">fasen: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="fae9f-107">phases : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="fae9f-108">Fasen van gedeeltelijke reflecties</span><span class="sxs-lookup"><span data-stu-id="fae9f-108">Phases of partial reflections</span></span>


### <a name="startstatereflection--reflectionoracle"></a><span data-ttu-id="fae9f-109">startStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="fae9f-109">startStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="fae9f-110">Reflectie operator over begin status</span><span class="sxs-lookup"><span data-stu-id="fae9f-110">Reflection operator about start state</span></span>


### <a name="targetstatereflection--reflectionoracle"></a><span data-ttu-id="fae9f-111">targetStateReflection: [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span><span class="sxs-lookup"><span data-stu-id="fae9f-111">targetStateReflection : [ReflectionOracle](xref:Microsoft.Quantum.Oracles.ReflectionOracle)</span></span>

<span data-ttu-id="fae9f-112">Reflectie operator over doel status</span><span class="sxs-lookup"><span data-stu-id="fae9f-112">Reflection operator about target state</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="fae9f-113">Output: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="fae9f-113">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="fae9f-114">Een bewerking waarbij amplitude versterking door gedeeltelijke reflecties wordt geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="fae9f-114">An operation that implements amplitude amplification by partial reflections.</span></span>

## <a name="remarks"></a><span data-ttu-id="fae9f-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="fae9f-115">Remarks</span></span>

<span data-ttu-id="fae9f-116">Amplitude versterking is een speciaal geval van een obliviouse amplitude versterking waarbij er geen systeem qubits is en de Oblivious Oracle is ingesteld op identiteit.</span><span class="sxs-lookup"><span data-stu-id="fae9f-116">Amplitude amplification is a special case of oblivious amplitude amplification where there are no system qubits and the oblivious oracle is set to identity.</span></span>
<span data-ttu-id="fae9f-117">In de meeste gevallen `startQubits` wordt geïnitialiseerd in de status $ \ket{\text{start}} \_ $1, de $-$1-eigenstate van `startStateReflection` .</span><span class="sxs-lookup"><span data-stu-id="fae9f-117">In most cases, `startQubits` is initialized in the state $\ket{\text{start}}\_1$, which is the $-1$ eigenstate of `startStateReflection`.</span></span>