---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorI
title: De functie ExtendedGreatestCommonDivisorI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorI
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 8cb21ae5052ae6c5a8aed8be71d6bd3d32034272
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708532"
---
# <a name="extendedgreatestcommondivisori-function"></a><span data-ttu-id="eab50-102">De functie ExtendedGreatestCommonDivisorI</span><span class="sxs-lookup"><span data-stu-id="eab50-102">ExtendedGreatestCommonDivisorI function</span></span>

<span data-ttu-id="eab50-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="eab50-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="eab50-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="eab50-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="eab50-105">Hiermee wordt een tuple $ (u, v) $ zodanig berekend dat $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $, waarbij $ \operatorname{GCD} $ $a $ grootste gemene deler van $a $ en $b $ is.</span><span class="sxs-lookup"><span data-stu-id="eab50-105">Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="eab50-106">De GCD is altijd positief.</span><span class="sxs-lookup"><span data-stu-id="eab50-106">The GCD is always positive.</span></span>

```qsharp
function ExtendedGreatestCommonDivisorI (a : Int, b : Int) : (Int, Int)
```


## <a name="input"></a><span data-ttu-id="eab50-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="eab50-107">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="eab50-108">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eab50-108">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eab50-109">het eerste getal waarvan de uitgebreide grootste algemene deler wordt berekend</span><span class="sxs-lookup"><span data-stu-id="eab50-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--int"></a><span data-ttu-id="eab50-110">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="eab50-110">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="eab50-111">het tweede getal waarvan de uitgebreide grootste algemene deler wordt berekend</span><span class="sxs-lookup"><span data-stu-id="eab50-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--intint"></a><span data-ttu-id="eab50-112">Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int))</span><span class="sxs-lookup"><span data-stu-id="eab50-112">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))</span></span>

<span data-ttu-id="eab50-113">Tuple $ (u, v) $ met de eigenschap $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $.</span><span class="sxs-lookup"><span data-stu-id="eab50-113">Tuple $(u,v)$ with the property $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$.</span></span>

## <a name="references"></a><span data-ttu-id="eab50-114">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="eab50-114">References</span></span>

- <span data-ttu-id="eab50-115">Deze implementatie is gebaseerd op https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span><span class="sxs-lookup"><span data-stu-id="eab50-115">This implementation is according to https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span></span>