---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: De functie ContinuousUniformDistribution
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: c81eb433f50277c677756ee70d916f4856260c6d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842318"
---
# <a name="continuousuniformdistribution-function"></a><span data-ttu-id="1d9d7-102">De functie ContinuousUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="1d9d7-102">ContinuousUniformDistribution function</span></span>

<span data-ttu-id="1d9d7-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="1d9d7-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="1d9d7-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="1d9d7-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="1d9d7-105">Retourneert een uniforme distributie over een opgegeven inclusief interval.</span><span class="sxs-lookup"><span data-stu-id="1d9d7-105">Returns a uniform distribution over a given inclusive interval.</span></span>

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a><span data-ttu-id="1d9d7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="1d9d7-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="1d9d7-107">min: [dubbele](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1d9d7-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1d9d7-108">Het kleinste reële getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="1d9d7-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="1d9d7-109">maximum: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="1d9d7-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="1d9d7-110">Het grootste reële getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="1d9d7-110">The largest real number to be drawn.</span></span>



## <a name="output--continuousdistribution"></a><span data-ttu-id="1d9d7-111">Uitvoer: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span><span class="sxs-lookup"><span data-stu-id="1d9d7-111">Output : [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)</span></span>

<span data-ttu-id="1d9d7-112">Een distributie waarvan de wille keurige variates reële getallen in het inclusieve interval zijn, van `min` tot `max` met een uniforme kans.</span><span class="sxs-lookup"><span data-stu-id="1d9d7-112">A distribution whose random variates are real numbers in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="example"></a><span data-ttu-id="1d9d7-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="1d9d7-113">Example</span></span>

<span data-ttu-id="1d9d7-114">Met de volgende Q # fragment wordt wille keurig een hoek getekend tussen $0 $ en $2 \pi $:</span><span class="sxs-lookup"><span data-stu-id="1d9d7-114">The following Q# snippet randomly draws an angle between $0$ and $2 \pi$:</span></span>

```qsharp
let angleDistribution = ContinuousUniformDistribution(0.0, 2.0 * PI());
let angle = angleDistribution::Sample();
```

## <a name="remarks"></a><span data-ttu-id="1d9d7-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="1d9d7-115">Remarks</span></span>

<span data-ttu-id="1d9d7-116">Mislukt als `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="1d9d7-116">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="1d9d7-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1d9d7-117">See Also</span></span>

- [<span data-ttu-id="1d9d7-118">Micro soft. Quantum. DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="1d9d7-118">Microsoft.Quantum.DrawRandomDouble</span></span>](xref:Microsoft.Quantum.DrawRandomDouble)