---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: De functie CategoricalDistribution
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 2e3d9b17939d5a9a5bc5e7d89a843e0ff5a848ba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210247"
---
# <a name="categoricaldistribution-function"></a><span data-ttu-id="e7c64-102">De functie CategoricalDistribution</span><span class="sxs-lookup"><span data-stu-id="e7c64-102">CategoricalDistribution function</span></span>

<span data-ttu-id="e7c64-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="e7c64-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="e7c64-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="e7c64-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="e7c64-105">Retourneert een discrete categorische-distributie, waarbij de kans voor elk van een eindige lijst met gegeven uitkomsten expliciet is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="e7c64-105">Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.</span></span>

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="e7c64-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e7c64-106">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="e7c64-107">tests: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="e7c64-107">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="e7c64-108">De kansen voor elk resultaat van de categorische-distributie.</span><span class="sxs-lookup"><span data-stu-id="e7c64-108">The probabilities for each outcome from the categorical distribution.</span></span>
<span data-ttu-id="e7c64-109">Deze waarschijnlijkheden mogen niet worden genormaliseerd, maar moeten allemaal niet-negatief zijn.</span><span class="sxs-lookup"><span data-stu-id="e7c64-109">These probabilities may not be normalized, but must all be non-negative.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="e7c64-110">Uitvoer: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="e7c64-110">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="e7c64-111">De index `i` met de waarschijnlijkheid `probs[i] / sum` , waarbij `sum` de som van de `probs` gegeven door is `Fold(PlusD, 0.0, probs)` .</span><span class="sxs-lookup"><span data-stu-id="e7c64-111">The index `i` with probability `probs[i] / sum`, where `sum` is the sum of `probs` given by `Fold(PlusD, 0.0, probs)`.</span></span>