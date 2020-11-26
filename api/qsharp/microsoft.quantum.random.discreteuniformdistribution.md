---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: De functie DiscreteUniformDistribution
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: 08a62805f59df339ef6b91dff802c40c407808f4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193009"
---
# <a name="discreteuniformdistribution-function"></a><span data-ttu-id="13b65-102">De functie DiscreteUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="13b65-102">DiscreteUniformDistribution function</span></span>

<span data-ttu-id="13b65-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="13b65-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="13b65-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="13b65-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="13b65-105">Retourneert een uniforme distributie over een opgegeven inclusief bereik.</span><span class="sxs-lookup"><span data-stu-id="13b65-105">Returns a uniform distribution over a given inclusive range.</span></span>

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="13b65-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="13b65-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="13b65-107">min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="13b65-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="13b65-108">Het kleinste gehele getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="13b65-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="13b65-109">Max.: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="13b65-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="13b65-110">Het grootste gehele getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="13b65-110">The largest integer to be drawn.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="13b65-111">Uitvoer: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="13b65-111">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="13b65-112">Een distributie waarvan de wille keurige variates gehele getallen in het inclusieve bereik zijn van `min` tot `max` met een uniforme kans.</span><span class="sxs-lookup"><span data-stu-id="13b65-112">A distribution whose random variates are integers in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="13b65-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="13b65-113">Remarks</span></span>

<span data-ttu-id="13b65-114">Mislukt als `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="13b65-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="13b65-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="13b65-115">See Also</span></span>

- [<span data-ttu-id="13b65-116">Micro soft. Quantum. DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="13b65-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)