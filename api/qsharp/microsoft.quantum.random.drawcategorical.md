---
uid: Microsoft.Quantum.Random.DrawCategorical
title: Bewerking DrawCategorical
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawCategorical
qsharp.summary: Draws a random sample from a categorical distribution specified by a list of probablities.
ms.openlocfilehash: a9fe1b08e80abc65a5c4b803f0cb8a5e7a62759c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851154"
---
# <a name="drawcategorical-operation"></a><span data-ttu-id="33943-102">Bewerking DrawCategorical</span><span class="sxs-lookup"><span data-stu-id="33943-102">DrawCategorical operation</span></span>

<span data-ttu-id="33943-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="33943-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="33943-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="33943-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="33943-105">Hiermee wordt een wille keurig voor beeld getekend vanuit een categorische-distributie die is opgegeven door een lijst met probablities.</span><span class="sxs-lookup"><span data-stu-id="33943-105">Draws a random sample from a categorical distribution specified by a list of probablities.</span></span>

```qsharp
operation DrawCategorical (probs : Double[]) : Int
```


## <a name="description"></a><span data-ttu-id="33943-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="33943-106">Description</span></span>

<span data-ttu-id="33943-107">De kans dat een specifieke index wordt geselecteerd, is evenredig met de waarde van het matrix element bij die index.</span><span class="sxs-lookup"><span data-stu-id="33943-107">The probability of selecting a specific index is proportional to the value of the array element at that index.</span></span>
<span data-ttu-id="33943-108">Matrix elementen die gelijk zijn aan nul, worden genegeerd en hun indices worden nooit geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="33943-108">Array elements that are equal to zero are ignored and their indices are never returned.</span></span> <span data-ttu-id="33943-109">Als een matrix element kleiner dan nul is, of als er geen matrix element groter is dan nul, mislukt de bewerking.</span><span class="sxs-lookup"><span data-stu-id="33943-109">If any array element is less than zero, or if no array element is greater than zero, then the operation fails.</span></span>

## <a name="input"></a><span data-ttu-id="33943-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="33943-110">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="33943-111">tests: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="33943-111">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="33943-112">Een matrix met drijvende-komma getallen die in verhouding staan tot de kans dat elke index wordt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="33943-112">An array of floating-point numbers proportional to the probability of selecting each index.</span></span>



## <a name="output--int"></a><span data-ttu-id="33943-113">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="33943-113">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="33943-114">Een geheel getal $i $ met kans $ \Pr (i) = p_i/\ sum_i p_i $, waarbij $p _i $ het $i $ TH-element van is `probs` .</span><span class="sxs-lookup"><span data-stu-id="33943-114">An integer $i$ with probability $\Pr(i) = p_i / \sum_i p_i$, where $p_i$ is the $i$th element of `probs`.</span></span>

## <a name="see-also"></a><span data-ttu-id="33943-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="33943-115">See Also</span></span>

- [<span data-ttu-id="33943-116">Micro soft. Quantum. wille keurig. CategoricalDistribution</span><span class="sxs-lookup"><span data-stu-id="33943-116">Microsoft.Quantum.Random.CategoricalDistribution</span></span>](xref:Microsoft.Quantum.Random.CategoricalDistribution)