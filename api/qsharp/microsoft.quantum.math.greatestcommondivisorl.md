---
uid: Microsoft.Quantum.Math.GreatestCommonDivisorL
title: De functie GreatestCommonDivisorL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: GreatestCommonDivisorL
qsharp.summary: Computes the greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 1bd18758bb2dea8a4801cbfdf258d91f81c5d9a4
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96195504"
---
# <a name="greatestcommondivisorl-function"></a><span data-ttu-id="34e54-102">De functie GreatestCommonDivisorL</span><span class="sxs-lookup"><span data-stu-id="34e54-102">GreatestCommonDivisorL function</span></span>

<span data-ttu-id="34e54-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="34e54-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="34e54-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="34e54-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="34e54-105">Berekent de grootste gemene deler van $a $ en $b $.</span><span class="sxs-lookup"><span data-stu-id="34e54-105">Computes the greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="34e54-106">De GCD is altijd positief.</span><span class="sxs-lookup"><span data-stu-id="34e54-106">The GCD is always positive.</span></span>

```qsharp
function GreatestCommonDivisorL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="34e54-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="34e54-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="34e54-108">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="34e54-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="34e54-109">het eerste getal waarvan de uitgebreide grootste algemene deler wordt berekend</span><span class="sxs-lookup"><span data-stu-id="34e54-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--bigint"></a><span data-ttu-id="34e54-110">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="34e54-110">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="34e54-111">het tweede getal waarvan de uitgebreide grootste algemene deler wordt berekend</span><span class="sxs-lookup"><span data-stu-id="34e54-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--bigint"></a><span data-ttu-id="34e54-112">Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="34e54-112">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="34e54-113">Grootste gemene deler van $a $ en $b $</span><span class="sxs-lookup"><span data-stu-id="34e54-113">Greatest common divisor of $a$ and $b$</span></span>