---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Bewerking DrawRandomInt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: d9d8d9fbb25587ac5ccbd4edf0e555649380375f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708934"
---
# <a name="drawrandomint-operation"></a><span data-ttu-id="4419d-102">Bewerking DrawRandomInt</span><span class="sxs-lookup"><span data-stu-id="4419d-102">DrawRandomInt operation</span></span>

<span data-ttu-id="4419d-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="4419d-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="4419d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4419d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4419d-105">Hiermee wordt een wille keurig geheel getal in een opgegeven, inclusief bereik getekend.</span><span class="sxs-lookup"><span data-stu-id="4419d-105">Draws a random integer in a given inclusive range.</span></span>

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a><span data-ttu-id="4419d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="4419d-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="4419d-107">min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4419d-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4419d-108">Het kleinste gehele getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="4419d-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="4419d-109">Max.: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4419d-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4419d-110">Het grootste gehele getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="4419d-110">The largest integer to be drawn.</span></span>



## <a name="output--int"></a><span data-ttu-id="4419d-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="4419d-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="4419d-112">Een geheel getal in het inclusieve bereik van `min` tot `max` en met een uniforme kans.</span><span class="sxs-lookup"><span data-stu-id="4419d-112">An integer in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="4419d-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="4419d-113">Remarks</span></span>

<span data-ttu-id="4419d-114">Mislukt als `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="4419d-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="4419d-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="4419d-115">See Also</span></span>

- [<span data-ttu-id="4419d-116">Micro soft. Quantum. DiscreteUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="4419d-116">Microsoft.Quantum.DiscreteUniformDistribution</span></span>](xref:Microsoft.Quantum.DiscreteUniformDistribution)