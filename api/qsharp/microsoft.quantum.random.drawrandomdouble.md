---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: Bewerking DrawRandomDouble
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: d62416f4a222716edb9393fe4f43731d0e8aa9d3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192941"
---
# <a name="drawrandomdouble-operation"></a><span data-ttu-id="5f575-102">Bewerking DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="5f575-102">DrawRandomDouble operation</span></span>

<span data-ttu-id="5f575-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="5f575-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="5f575-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="5f575-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="5f575-105">Hiermee wordt een wille keurig reëel getal in een opgegeven inclusief interval getekend.</span><span class="sxs-lookup"><span data-stu-id="5f575-105">Draws a random real number in a given inclusive interval.</span></span>

```qsharp
operation DrawRandomDouble (min : Double, max : Double) : Double
```


## <a name="input"></a><span data-ttu-id="5f575-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5f575-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="5f575-107">min: [dubbele](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5f575-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5f575-108">Het kleinste reële getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="5f575-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="5f575-109">maximum: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5f575-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5f575-110">Het grootste reële getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="5f575-110">The largest real number to be drawn.</span></span>



## <a name="output--double"></a><span data-ttu-id="5f575-111">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="5f575-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="5f575-112">Een wille keurig reëel getal in het inclusieve interval van `min` tot `max` met een uniforme kans.</span><span class="sxs-lookup"><span data-stu-id="5f575-112">A random real number in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f575-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="5f575-113">Remarks</span></span>

<span data-ttu-id="5f575-114">Mislukt als `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="5f575-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f575-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5f575-115">See Also</span></span>

- [<span data-ttu-id="5f575-116">Micro soft. Quantum. ContinuousUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="5f575-116">Microsoft.Quantum.ContinuousUniformDistribution</span></span>](xref:Microsoft.Quantum.ContinuousUniformDistribution)