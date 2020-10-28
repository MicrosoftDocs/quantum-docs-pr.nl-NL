---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorL
title: De functie ExtendedGreatestCommonDivisorL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorL
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: e671405045d6d2587a8c6ccbac4ae3402f92f722
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708527"
---
# <a name="extendedgreatestcommondivisorl-function"></a><span data-ttu-id="03bd2-102">De functie ExtendedGreatestCommonDivisorL</span><span class="sxs-lookup"><span data-stu-id="03bd2-102">ExtendedGreatestCommonDivisorL function</span></span>

<span data-ttu-id="03bd2-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="03bd2-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="03bd2-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="03bd2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="03bd2-105">Hiermee wordt een tuple $ (u, v) $ zodanig berekend dat $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $, waarbij $ \operatorname{GCD} $ $a $ grootste gemene deler van $a $ en $b $ is.</span><span class="sxs-lookup"><span data-stu-id="03bd2-105">Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="03bd2-106">De GCD is altijd positief.</span><span class="sxs-lookup"><span data-stu-id="03bd2-106">The GCD is always positive.</span></span>

```qsharp
function ExtendedGreatestCommonDivisorL (a : BigInt, b : BigInt) : (BigInt, BigInt)
```


## <a name="input"></a><span data-ttu-id="03bd2-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="03bd2-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="03bd2-108">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="03bd2-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="03bd2-109">het eerste getal waarvan de uitgebreide grootste algemene deler wordt berekend</span><span class="sxs-lookup"><span data-stu-id="03bd2-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--bigint"></a><span data-ttu-id="03bd2-110">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="03bd2-110">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="03bd2-111">het tweede getal waarvan de uitgebreide grootste algemene deler wordt berekend</span><span class="sxs-lookup"><span data-stu-id="03bd2-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--bigintbigint"></a><span data-ttu-id="03bd2-112">Uitvoer: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="03bd2-112">Output : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>

<span data-ttu-id="03bd2-113">Tuple $ (u, v) $ met de eigenschap $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $.</span><span class="sxs-lookup"><span data-stu-id="03bd2-113">Tuple $(u,v)$ with the property $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$.</span></span>

## <a name="references"></a><span data-ttu-id="03bd2-114">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="03bd2-114">References</span></span>

- <span data-ttu-id="03bd2-115">Deze implementatie is gebaseerd op https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span><span class="sxs-lookup"><span data-stu-id="03bd2-115">This implementation is according to https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span></span>