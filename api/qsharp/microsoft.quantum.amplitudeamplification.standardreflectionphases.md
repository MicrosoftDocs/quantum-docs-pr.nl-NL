---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: De functie StandardReflectionPhases
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: 703b50d0186cd0f4eddb9a29fa3cffb2b746c8d6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843921"
---
# <a name="standardreflectionphases-function"></a><span data-ttu-id="7f420-102">De functie StandardReflectionPhases</span><span class="sxs-lookup"><span data-stu-id="7f420-102">StandardReflectionPhases function</span></span>

<span data-ttu-id="7f420-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="7f420-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="7f420-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7f420-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7f420-105">Berekent gedeeltelijke reflectie fasen voor standaard amplitude versterking.</span><span class="sxs-lookup"><span data-stu-id="7f420-105">Computes partial reflection phases for standard amplitude amplification.</span></span>

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="7f420-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="7f420-106">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="7f420-107">nIterations: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7f420-107">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7f420-108">Aantal amplitude versterkings herhalingen waarvoor gedeeltelijke reflectie fasen worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="7f420-108">Number of amplitude amplification iterations to generate partial reflection phases for.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="7f420-109">Uitvoer: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="7f420-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="7f420-110">Een bewerking waarmee fasen worden geïmplementeerd die zijn opgegeven als gedeeltelijke reflecties</span><span class="sxs-lookup"><span data-stu-id="7f420-110">An operation that implements phases specified as partial reflections</span></span>

## <a name="remarks"></a><span data-ttu-id="7f420-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="7f420-111">Remarks</span></span>

<span data-ttu-id="7f420-112">Alle fasen zijn $ \pi $, met uitzonde ring van de eerste reflectie over de begin status en de laatste reflectie over de doel status, die $0 $ zijn.</span><span class="sxs-lookup"><span data-stu-id="7f420-112">All phases are $\pi$, except for the first reflection about the start state and the last reflection about the target state, which are $0$.</span></span>