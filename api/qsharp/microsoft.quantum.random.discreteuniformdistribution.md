---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: De functie DiscreteUniformDistribution
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: f909e7def5439ec0feef4ca4dc0cf8ed12374dfe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853727"
---
# <a name="discreteuniformdistribution-function"></a><span data-ttu-id="3ea77-102">De functie DiscreteUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="3ea77-102">DiscreteUniformDistribution function</span></span>

<span data-ttu-id="3ea77-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="3ea77-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="3ea77-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="3ea77-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="3ea77-105">Retourneert een uniforme distributie over een opgegeven inclusief bereik.</span><span class="sxs-lookup"><span data-stu-id="3ea77-105">Returns a uniform distribution over a given inclusive range.</span></span>

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a><span data-ttu-id="3ea77-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="3ea77-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="3ea77-107">min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3ea77-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3ea77-108">Het kleinste gehele getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="3ea77-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="3ea77-109">Max.: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3ea77-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3ea77-110">Het grootste gehele getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="3ea77-110">The largest integer to be drawn.</span></span>



## <a name="output--discretedistribution"></a><span data-ttu-id="3ea77-111">Uitvoer: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span><span class="sxs-lookup"><span data-stu-id="3ea77-111">Output : [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)</span></span>

<span data-ttu-id="3ea77-112">Een distributie waarvan de wille keurige variates gehele getallen in het inclusieve bereik zijn van `min` tot `max` met een uniforme kans.</span><span class="sxs-lookup"><span data-stu-id="3ea77-112">A distribution whose random variates are integers in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="example"></a><span data-ttu-id="3ea77-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="3ea77-113">Example</span></span>

<span data-ttu-id="3ea77-114">Het volgende Q #-fragment rolt een wille keurige dobbel steen op met zes zijden:</span><span class="sxs-lookup"><span data-stu-id="3ea77-114">The following Q# snippet randomly rolls a six-sided die:</span></span>

```qsharp
let dieDistribution = DiscreteUniformDistribution(1, 6);
let dieRoll = dieDistribution::Sample();
```

## <a name="remarks"></a><span data-ttu-id="3ea77-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="3ea77-115">Remarks</span></span>

<span data-ttu-id="3ea77-116">Mislukt als `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="3ea77-116">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="3ea77-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3ea77-117">See Also</span></span>

- [<span data-ttu-id="3ea77-118">Micro soft. Quantum. DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="3ea77-118">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)