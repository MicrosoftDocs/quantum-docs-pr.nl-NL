---
uid: Microsoft.Quantum.Random.DrawRandomInt
title: Bewerking DrawRandomInt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DrawRandomInt
qsharp.summary: Draws a random integer in a given inclusive range.
ms.openlocfilehash: ebed7f52b7c4a8c538ed9d718c486b5aa94a0327
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851143"
---
# <a name="drawrandomint-operation"></a><span data-ttu-id="07a83-102">Bewerking DrawRandomInt</span><span class="sxs-lookup"><span data-stu-id="07a83-102">DrawRandomInt operation</span></span>

<span data-ttu-id="07a83-103">Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)</span><span class="sxs-lookup"><span data-stu-id="07a83-103">Namespace: [Microsoft.Quantum.Random](xref:Microsoft.Quantum.Random)</span></span>

<span data-ttu-id="07a83-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="07a83-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="07a83-105">Hiermee wordt een wille keurig geheel getal in een opgegeven, inclusief bereik getekend.</span><span class="sxs-lookup"><span data-stu-id="07a83-105">Draws a random integer in a given inclusive range.</span></span>

```qsharp
operation DrawRandomInt (min : Int, max : Int) : Int
```


## <a name="input"></a><span data-ttu-id="07a83-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="07a83-106">Input</span></span>

### <a name="min--int"></a><span data-ttu-id="07a83-107">min: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="07a83-107">min : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="07a83-108">Het kleinste gehele getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="07a83-108">The smallest integer to be drawn.</span></span>


### <a name="max--int"></a><span data-ttu-id="07a83-109">Max.: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="07a83-109">max : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="07a83-110">Het grootste gehele getal dat moet worden getekend.</span><span class="sxs-lookup"><span data-stu-id="07a83-110">The largest integer to be drawn.</span></span>



## <a name="output--int"></a><span data-ttu-id="07a83-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="07a83-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="07a83-112">Een geheel getal in het inclusieve bereik van `min` tot `max` en met een uniforme kans.</span><span class="sxs-lookup"><span data-stu-id="07a83-112">An integer in the inclusive range from `min` to `max` with uniform probability.</span></span>

## <a name="example"></a><span data-ttu-id="07a83-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="07a83-113">Example</span></span>

<span data-ttu-id="07a83-114">Het volgende Q #-fragment rolt een wille keurige dobbel steen op met zes zijden:</span><span class="sxs-lookup"><span data-stu-id="07a83-114">The following Q# snippet randomly rolls a six-sided die:</span></span>

```qsharp
let roll = DrawRandomInt(1, 6);
```

## <a name="remarks"></a><span data-ttu-id="07a83-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="07a83-115">Remarks</span></span>

<span data-ttu-id="07a83-116">Mislukt als `max <= min` .</span><span class="sxs-lookup"><span data-stu-id="07a83-116">Fails if `max <= min`.</span></span>

## <a name="see-also"></a><span data-ttu-id="07a83-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="07a83-117">See Also</span></span>

- [<span data-ttu-id="07a83-118">Micro soft. Quantum. DiscreteUniformDistribution</span><span class="sxs-lookup"><span data-stu-id="07a83-118">Microsoft.Quantum.DiscreteUniformDistribution</span></span>](xref:Microsoft.Quantum.DiscreteUniformDistribution)