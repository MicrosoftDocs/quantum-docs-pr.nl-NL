---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: De functie DiscreteUniformDistribution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: 5e93c66d891d9b6aec548c0cf266df35e6090c92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706725"
---
# <a name="discreteuniformdistribution-function"></a><span data-ttu-id="8bfc0-102">De functie DiscreteUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="8bfc0-102">DiscreteUniformDistribution function</span></span>

<span data-ttu-id="8bfc0-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="8bfc0-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="8bfc0-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8bfc0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8bfc0-105">Retourneert een uniforme distributie over een opgegeven inclusief bereik.</span><span class="sxs-lookup"><span data-stu-id="8bfc0-105">Returns a uniform distribution over a given inclusive range.</span></span>

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="8bfc0-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="8bfc0-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="8bfc0-107">min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8bfc0-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8bfc0-108">Het kleinste gehele getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="8bfc0-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="8bfc0-109">Max.: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="8bfc0-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="8bfc0-110">Het grootste gehele getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="8bfc0-110">The largest integer to be drawn.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="8bfc0-111">Uitvoer: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="8bfc0-111">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="8bfc0-112">Een distributie waarvan de wille keurige variates gehele getallen in het inclusieve bereik zijn van `min` tot `max` met een uniforme kans.</span><span class="sxs-lookup"><span data-stu-id="8bfc0-112">A distribution whose random variates are integers in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="8bfc0-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="8bfc0-113">Remarks</span></span>

<span data-ttu-id="8bfc0-114">Mislukt als `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="8bfc0-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="8bfc0-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8bfc0-115">See Also</span></span>

- [<span data-ttu-id="8bfc0-116">Micro soft. Quantum. DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="8bfc0-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)