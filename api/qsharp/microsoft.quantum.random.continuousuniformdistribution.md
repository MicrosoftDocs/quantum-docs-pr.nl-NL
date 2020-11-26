---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: De functie ContinuousUniformDistribution
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: a3911fe9962ce18daa239de0272c53d83344134a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193077"
---
# <a name="continuousuniformdistribution-function"></a><span data-ttu-id="542a5-102">De functie ContinuousUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="542a5-102">ContinuousUniformDistribution function</span></span>

<span data-ttu-id="542a5-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="542a5-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="542a5-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="542a5-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="542a5-105">Retourneert een uniforme distributie over een opgegeven inclusief interval.</span><span class="sxs-lookup"><span data-stu-id="542a5-105">Returns a uniform distribution over a given inclusive interval.</span></span>

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="542a5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="542a5-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="542a5-107">min: [dubbele](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="542a5-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="542a5-108">Het kleinste reële getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="542a5-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="542a5-109">maximum: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="542a5-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="542a5-110">Het grootste reële getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="542a5-110">The largest real number to be drawn.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="542a5-111">Uitvoer: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="542a5-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="542a5-112">Een distributie waarvan de wille keurige variates reële getallen in het inclusieve interval zijn, van `min` tot `max` met een uniforme kans.</span><span class="sxs-lookup"><span data-stu-id="542a5-112">A distribution whose random variates are real numbers in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="542a5-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="542a5-113">Remarks</span></span>

<span data-ttu-id="542a5-114">Mislukt als `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="542a5-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="542a5-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="542a5-115">See Also</span></span>

- [<span data-ttu-id="542a5-116">Micro soft. Quantum. DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="542a5-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)