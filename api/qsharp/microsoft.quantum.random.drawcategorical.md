---
uid: Microsoft.Quantum.Random.DrawCategorical
title: Bewerking DrawCategorical
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawCategorical
qsharp.summary: Draws a random sample from a categorical distribution specified by a list of probablities.
ms.openlocfilehash: fdc5ae3a9341cb11e8fda129bdd030289b6c99c2
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706717"
---
# <a name="drawcategorical-operation"></a><span data-ttu-id="58bf9-102">Bewerking DrawCategorical</span><span class="sxs-lookup"><span data-stu-id="58bf9-102">DrawCategorical operation</span></span>

<span data-ttu-id="58bf9-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="58bf9-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="58bf9-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="58bf9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="58bf9-105">Hiermee wordt een wille keurig voor beeld getekend vanuit een categorische-distributie die is opgegeven door een lijst met probablities.</span><span class="sxs-lookup"><span data-stu-id="58bf9-105">Draws a random sample from a categorical distribution specified by a list of probablities.</span></span>

```qsharp
operation DrawCategorical (probs : Double[]) : Int
```


## <a name="description"></a><span data-ttu-id="58bf9-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="58bf9-106">Description</span></span>

<span data-ttu-id="58bf9-107">De kans dat een specifieke index wordt geselecteerd, is evenredig met de waarde van het matrix element bij die index.</span><span class="sxs-lookup"><span data-stu-id="58bf9-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span>
<span data-ttu-id="58bf9-108">Matrix elementen die gelijk zijn aan nul, worden genegeerd en hun indices worden nooit geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="58bf9-108">Array elements that are equal to zero are ignored and their indices are never returned.</span></span> <span data-ttu-id="58bf9-109">Als een matrix element kleiner dan nul is, of als er geen matrix element groter is dan nul, mislukt de bewerking.</span><span class="sxs-lookup"><span data-stu-id="58bf9-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>

## <a name="input"></a><span data-ttu-id="58bf9-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="58bf9-110">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="58bf9-111">tests: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="58bf9-111">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="58bf9-112">Een matrix met drijvende-komma getallen die in verhouding staan tot de kans dat elke index wordt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="58bf9-112">An array of floating-point numbers proportional to the probability of selecting each index.</span></span>



## <a name="output--int"></a><span data-ttu-id="58bf9-113">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="58bf9-113">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="58bf9-114">Een geheel getal $i $ met kans $ \Pr (i) = p_i/\ sum_i p_i $, waarbij $p _i $ het $i $ TH-element van is `probs` .</span><span class="sxs-lookup"><span data-stu-id="58bf9-114">An integer $i$ with probability $\Pr(i) = p_i / \sum_i p_i$, where $p_i$ is the $i$th element of `probs`.</span></span>

## <a name="see-also"></a><span data-ttu-id="58bf9-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="58bf9-115">See Also</span></span>

- [<span data-ttu-id="58bf9-116">Micro soft. Quantum. wille keurig. CategoricalDistribution</span><span class="sxs-lookup"><span data-stu-id="58bf9-116">Microsoft.Quantum.Random.CategoricalDistribution</span></span>](xref:Microsoft.Quantum.Random.CategoricalDistribution)