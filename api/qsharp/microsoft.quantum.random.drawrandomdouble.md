---
uid: Microsoft.Quantum.Random.DrawRandomDouble
title: Bewerking DrawRandomDouble
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomDouble
qsharp.summary: Draws a random real number in a given inclusive interval.
ms.openlocfilehash: 792e9c714b761b48618aec2091e167a359c2b522
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847614"
---
# <a name="drawrandomdouble-operation"></a><span data-ttu-id="56723-102">Bewerking DrawRandomDouble</span><span class="sxs-lookup"><span data-stu-id="56723-102">DrawRandomDouble operation</span></span>

<span data-ttu-id="56723-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="56723-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="56723-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="56723-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="56723-105">Hiermee wordt een wille keurig reëel getal in een opgegeven inclusief interval getekend.</span><span class="sxs-lookup"><span data-stu-id="56723-105">Draws a random real number in a given inclusive interval.</span></span>

```qsharp
operation DrawRandomDouble (min : Double, max : Double) : Double
```


## <a name="input"></a><span data-ttu-id="56723-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="56723-106">Input</span></span>

### <a name="min--double"></a><span data-ttu-id="56723-107">min: [dubbele](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="56723-107">min : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="56723-108">Het kleinste reële getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="56723-108">The smallest real number to be drawn.</span></span>


### <a name="max--double"></a><span data-ttu-id="56723-109">maximum: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="56723-109">max : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="56723-110">Het grootste reële getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="56723-110">The largest real number to be drawn.</span></span>



## <a name="output--double"></a><span data-ttu-id="56723-111">Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="56723-111">Output : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="56723-112">Een wille keurig reëel getal in het inclusieve interval van `min` tot `max` met een uniforme kans.</span><span class="sxs-lookup"><span data-stu-id="56723-112">A random real number in the inclusive interval from `min` to `max` with uniform probability.</span></span>

## <a name="example"></a><span data-ttu-id="56723-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="56723-113">Example</span></span>

<span data-ttu-id="56723-114">Met de volgende Q # fragment wordt wille keurig een hoek getekend tussen $0 $ en $2 \pi $:</span><span class="sxs-lookup"><span data-stu-id="56723-114">The following Q# snippet randomly draws an angle between $0$ and $2 \pi$:</span></span>

```qsharp
let angle = DrawRandomDouble(0.0, 2.0 * PI());
```

## <a name="remarks"></a><span data-ttu-id="56723-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="56723-115">Remarks</span></span>

<span data-ttu-id="56723-116">Mislukt als `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="56723-116">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="56723-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="56723-117">See Also</span></span>

- [<span data-ttu-id="56723-118">Micro soft. Quantum. ContinuousUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="56723-118">Microsoft.Quantum.ContinuousUniformDistribution</span></span>](xref:Microsoft.Quantum.ContinuousUniformDistribution)