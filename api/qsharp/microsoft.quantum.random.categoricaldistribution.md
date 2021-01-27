---
uid: Microsoft.Quantum.Random.CategoricalDistribution
title: De functie CategoricalDistribution
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: CategoricalDistribution
qsharp.summary: Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.
ms.openlocfilehash: 754ada71078bd5446f78885ace31d92dce6bf1a4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842352"
---
# <a name="categoricaldistribution-function"></a><span data-ttu-id="c5bfc-102">De functie CategoricalDistribution</span><span class="sxs-lookup"><span data-stu-id="c5bfc-102">CategoricalDistribution function</span></span>

<span data-ttu-id="c5bfc-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="c5bfc-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="c5bfc-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c5bfc-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c5bfc-105">Retourneert een discrete categorische-distributie, waarbij de kans voor elk van een eindige lijst met gegeven uitkomsten expliciet is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="c5bfc-105">Returns a discrete categorical distribution, in which the probability for each of a finite list of given outcomes is explicitly specified.</span></span>

```qsharp
function CategoricalDistribution (probs : Double[]) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="c5bfc-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c5bfc-106">Input</span></span>

### <a name="probs--double"></a><span data-ttu-id="c5bfc-107">tests: [dubbele](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="c5bfc-107">probs : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="c5bfc-108">De kansen voor elk resultaat van de categorische-distributie.</span><span class="sxs-lookup"><span data-stu-id="c5bfc-108">The probabilities for each outcome from the categorical distribution.</span></span>
<span data-ttu-id="c5bfc-109">Deze waarschijnlijkheden mogen niet worden genormaliseerd, maar moeten allemaal niet-negatief zijn.</span><span class="sxs-lookup"><span data-stu-id="c5bfc-109">These probabilities may not be normalized, but must all be non-negative.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="c5bfc-110">Uitvoer: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="c5bfc-110">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="c5bfc-111">De index `i` met de waarschijnlijkheid `probs[i] / sum` , waarbij `sum` de som van de `probs` gegeven door is `Fold(PlusD, 0.0, probs)` .</span><span class="sxs-lookup"><span data-stu-id="c5bfc-111">The index `i` with probability `probs[i] / sum`, where `sum` is the sum of `probs` given by `Fold(PlusD, 0.0, probs)`.</span></span>

## <a name="example"></a><span data-ttu-id="c5bfc-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="c5bfc-112">Example</span></span>

<span data-ttu-id="c5bfc-113">Met de volgende Q #-code wordt 0 weer gegeven met een kans van 30% en 1 met een waarschijnlijkheids gewicht van 70%:</span><span class="sxs-lookup"><span data-stu-id="c5bfc-113">The following Q# code will display 0 with probability 30% and 1 with probability 70%:</span></span>

```qsharp
let dist = CategoricalDistribution([0.3, 0.7]);
Message($"Got sample: {dist::Sample()}");
```