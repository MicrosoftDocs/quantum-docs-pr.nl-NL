---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Bewerking DrawRandomInt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: f7b6cb75f761e4c45295245ed4bd4fb82c592809
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192907"
---
# <a name="drawrandomint-operation"></a><span data-ttu-id="28822-102">Bewerking DrawRandomInt</span><span class="sxs-lookup"><span data-stu-id="28822-102">DrawRandomInt operation</span></span>

<span data-ttu-id="28822-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="28822-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="28822-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="28822-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="28822-105">Hiermee wordt een wille keurig geheel getal in een opgegeven, inclusief bereik getekend.</span><span class="sxs-lookup"><span data-stu-id="28822-105">Draws a random integer in a given inclusive range.</span></span>

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a><span data-ttu-id="28822-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="28822-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="28822-107">min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="28822-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="28822-108">Het kleinste gehele getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="28822-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="28822-109">Max.: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="28822-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="28822-110">Het grootste gehele getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="28822-110">The largest integer to be drawn.</span></span>



## <a name="output--int"></a><span data-ttu-id="28822-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="28822-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="28822-112">Een geheel getal in het inclusieve bereik van `min` tot `max` en met een uniforme kans.</span><span class="sxs-lookup"><span data-stu-id="28822-112">An integer in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="remarks"></a><span data-ttu-id="28822-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="28822-113">Remarks</span></span>

<span data-ttu-id="28822-114">Mislukt als `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="28822-114">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="28822-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="28822-115">See Also</span></span>

- [<span data-ttu-id="28822-116">Micro soft. Quantum. DiscreteUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="28822-116">Microsoft.Quantum.DiscreteUniformDistribution</span></span>](xref:Microsoft.Quantum.DiscreteUniformDistribution)