---
uid: Microsoft.Quantum.Math.ExtendedGreatestCommonDivisorL
title: De functie ExtendedGreatestCommonDivisorL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExtendedGreatestCommonDivisorL
qsharp.summary: Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: abbbd367859952180f181a245ca0754646529b18
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210706"
---
# <a name="extendedgreatestcommondivisorl-function"></a><span data-ttu-id="fb2ad-102">De functie ExtendedGreatestCommonDivisorL</span><span class="sxs-lookup"><span data-stu-id="fb2ad-102">ExtendedGreatestCommonDivisorL function</span></span>

<span data-ttu-id="fb2ad-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="fb2ad-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="fb2ad-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fb2ad-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fb2ad-105">Hiermee wordt een tuple $ (u, v) $ zodanig berekend dat $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $, waarbij $ \operatorname{GCD} $ $a $ grootste gemene deler van $a $ en $b $ is.</span><span class="sxs-lookup"><span data-stu-id="fb2ad-105">Computes a tuple $(u,v)$ such that $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$, where $\operatorname{GCD}$ is $a$ greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="fb2ad-106">De GCD is altijd positief.</span><span class="sxs-lookup"><span data-stu-id="fb2ad-106">The GCD is always positive.</span></span>

```qsharp
function ExtendedGreatestCommonDivisorL (a : BigInt, b : BigInt) : (BigInt, BigInt)
```


## <a name="input"></a><span data-ttu-id="fb2ad-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="fb2ad-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="fb2ad-108">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="fb2ad-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="fb2ad-109">het eerste getal waarvan de uitgebreide grootste algemene deler wordt berekend</span><span class="sxs-lookup"><span data-stu-id="fb2ad-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--bigint"></a><span data-ttu-id="fb2ad-110">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="fb2ad-110">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="fb2ad-111">het tweede getal waarvan de uitgebreide grootste algemene deler wordt berekend</span><span class="sxs-lookup"><span data-stu-id="fb2ad-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--bigintbigint"></a><span data-ttu-id="fb2ad-112">Uitvoer: ([bigint](xref:microsoft.quantum.lang-ref.bigint),[bigint](xref:microsoft.quantum.lang-ref.bigint))</span><span class="sxs-lookup"><span data-stu-id="fb2ad-112">Output : ([BigInt](xref:microsoft.quantum.lang-ref.bigint),[BigInt](xref:microsoft.quantum.lang-ref.bigint))</span></span>

<span data-ttu-id="fb2ad-113">Tuple $ (u, v) $ met de eigenschap $u \cdot a + v \cdot b = \operatorname{GCD} (a, b) $.</span><span class="sxs-lookup"><span data-stu-id="fb2ad-113">Tuple $(u,v)$ with the property $u \cdot a + v \cdot b = \operatorname{GCD}(a, b)$.</span></span>

## <a name="references"></a><span data-ttu-id="fb2ad-114">Referenties</span><span class="sxs-lookup"><span data-stu-id="fb2ad-114">References</span></span>

- <span data-ttu-id="fb2ad-115">Deze implementatie is gebaseerd op https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span><span class="sxs-lookup"><span data-stu-id="fb2ad-115">This implementation is according to https://en.wikipedia.org/wiki/Extended_Euclidean_algorithm</span></span>