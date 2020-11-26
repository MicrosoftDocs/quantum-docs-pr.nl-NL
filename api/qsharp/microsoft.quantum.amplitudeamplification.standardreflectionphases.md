---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: De functie StandardReflectionPhases
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: 316c8f22a16859ebb439824eda9a5aa02c750b5d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96191122"
---
# <a name="standardreflectionphases-function"></a><span data-ttu-id="ef6ce-102">De functie StandardReflectionPhases</span><span class="sxs-lookup"><span data-stu-id="ef6ce-102">StandardReflectionPhases function</span></span>

<span data-ttu-id="ef6ce-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="ef6ce-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="ef6ce-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ef6ce-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ef6ce-105">Berekent gedeeltelijke reflectie fasen voor standaard amplitude versterking.</span><span class="sxs-lookup"><span data-stu-id="ef6ce-105">Computes partial reflection phases for standard amplitude amplification.</span></span>

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="ef6ce-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ef6ce-106">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="ef6ce-107">nIterations: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="ef6ce-107">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="ef6ce-108">Aantal amplitude versterkings herhalingen waarvoor gedeeltelijke reflectie fasen worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="ef6ce-108">Number of amplitude amplification iterations to generate partial reflection phases for.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="ef6ce-109">Uitvoer: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="ef6ce-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="ef6ce-110">Een bewerking waarmee fasen worden geïmplementeerd die zijn opgegeven als gedeeltelijke reflecties</span><span class="sxs-lookup"><span data-stu-id="ef6ce-110">An operation that implements phases specified as partial reflections</span></span>

## <a name="remarks"></a><span data-ttu-id="ef6ce-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="ef6ce-111">Remarks</span></span>

<span data-ttu-id="ef6ce-112">Alle fasen zijn $ \pi $, met uitzonde ring van de eerste reflectie over de begin status en de laatste reflectie over de doel status, die $0 $ zijn.</span><span class="sxs-lookup"><span data-stu-id="ef6ce-112">All phases are $\pi$, except for the first reflection about the start state and the last reflection about the target state, which are $0$.</span></span>