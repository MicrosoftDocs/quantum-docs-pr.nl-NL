---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: De functie StandardReflectionPhases
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: c189b34b641989ab458986fb3f2872759b949be5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707680"
---
# <a name="standardreflectionphases-function"></a><span data-ttu-id="91677-102">De functie StandardReflectionPhases</span><span class="sxs-lookup"><span data-stu-id="91677-102">StandardReflectionPhases function</span></span>

<span data-ttu-id="91677-103">Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span><span class="sxs-lookup"><span data-stu-id="91677-103">Namespace: [Microsoft.Quantum.AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)</span></span>

<span data-ttu-id="91677-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="91677-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="91677-105">Berekent gedeeltelijke reflectie fasen voor standaard amplitude versterking.</span><span class="sxs-lookup"><span data-stu-id="91677-105">Computes partial reflection phases for standard amplitude amplification.</span></span>

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a><span data-ttu-id="91677-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="91677-106">Input</span></span>

### <a name="niterations--int"></a><span data-ttu-id="91677-107">nIterations: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="91677-107">nIterations : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="91677-108">Aantal amplitude versterkings herhalingen waarvoor gedeeltelijke reflectie fasen worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="91677-108">Number of amplitude amplification iterations to generate partial reflection phases for.</span></span>



## <a name="output--reflectionphases"></a><span data-ttu-id="91677-109">Uitvoer: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span><span class="sxs-lookup"><span data-stu-id="91677-109">Output : [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)</span></span>

<span data-ttu-id="91677-110">Een bewerking waarmee fasen worden geïmplementeerd die zijn opgegeven als gedeeltelijke reflecties</span><span class="sxs-lookup"><span data-stu-id="91677-110">An operation that implements phases specified as partial reflections</span></span>

## <a name="remarks"></a><span data-ttu-id="91677-111">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="91677-111">Remarks</span></span>

<span data-ttu-id="91677-112">Alle fasen zijn $ \pi $, met uitzonde ring van de eerste reflectie over de begin status en de laatste reflectie over de doel status, die $0 $ zijn.</span><span class="sxs-lookup"><span data-stu-id="91677-112">All phases are $\pi$, except for the first reflection about the start state and the last reflection about the target state, which are $0$.</span></span>