---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: De functie ContinuousUniformDistribution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: 74300efb10ba7b5aa006f0b1b6aafde0da840f00
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701235"
---
# <a name="continuousuniformdistribution-function"></a><span data-ttu-id="d176f-102">De functie ContinuousUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="d176f-102">ContinuousUniformDistribution function</span></span>

<span data-ttu-id="d176f-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="d176f-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="d176f-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d176f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d176f-105">Retourneert een uniforme distributie over een opgegeven inclusief interval.</span><span class="sxs-lookup"><span data-stu-id="d176f-105">Returns a uniform distribution over a given inclusive interval.</span></span>

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="d176f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d176f-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="d176f-107">min: [dubbele](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d176f-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d176f-108">Het kleinste reële getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="d176f-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="d176f-109">maximum: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d176f-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d176f-110">Het grootste reële getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="d176f-110">The largest real number to be drawn.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="d176f-111">Uitvoer: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="d176f-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="d176f-112">Een distributie waarvan de wille keurige variates reële getallen in het inclusieve interval zijn, van `min` tot `max` met een uniforme kans.</span><span class="sxs-lookup"><span data-stu-id="d176f-112">A distribution whose random variates are real numbers in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="d176f-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d176f-113">Remarks</span></span>

<span data-ttu-id="d176f-114">Mislukt als `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="d176f-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="d176f-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d176f-115">See Also</span></span>

- [<span data-ttu-id="d176f-116">Micro soft. Quantum. DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="d176f-116">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)