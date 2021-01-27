---
uid: Microsoft.Quantum.Math.GreatestCommonDivisorL
title: De functie GreatestCommonDivisorL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: GreatestCommonDivisorL
qsharp.summary: Computes the greatest common divisor of $a$ and $b$. The GCD is always positive.
ms.openlocfilehash: 0f545f7888f5a9a353cc6000a12988648ac82dd8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856380"
---
# <a name="greatestcommondivisorl-function"></a><span data-ttu-id="2f057-102">De functie GreatestCommonDivisorL</span><span class="sxs-lookup"><span data-stu-id="2f057-102">GreatestCommonDivisorL function</span></span>

<span data-ttu-id="2f057-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="2f057-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="2f057-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2f057-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2f057-105">Berekent de grootste gemene deler van $a $ en $b $.</span><span class="sxs-lookup"><span data-stu-id="2f057-105">Computes the greatest common divisor of $a$ and $b$.</span></span> <span data-ttu-id="2f057-106">De GCD is altijd positief.</span><span class="sxs-lookup"><span data-stu-id="2f057-106">The GCD is always positive.</span></span>

```qsharp
function GreatestCommonDivisorL (a : BigInt, b : BigInt) : BigInt
```


## <a name="input"></a><span data-ttu-id="2f057-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="2f057-107">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="2f057-108">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2f057-108">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2f057-109">het eerste getal waarvan de uitgebreide grootste algemene deler wordt berekend</span><span class="sxs-lookup"><span data-stu-id="2f057-109">the first number of which extended greatest common divisor is being computed</span></span>


### <a name="b--bigint"></a><span data-ttu-id="2f057-110">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2f057-110">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2f057-111">het tweede getal waarvan de uitgebreide grootste algemene deler wordt berekend</span><span class="sxs-lookup"><span data-stu-id="2f057-111">the second number of which extended greatest common divisor is being computed</span></span>



## <a name="output--bigint"></a><span data-ttu-id="2f057-112">Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2f057-112">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2f057-113">Grootste gemene deler van $a $ en $b $</span><span class="sxs-lookup"><span data-stu-id="2f057-113">Greatest common divisor of $a$ and $b$</span></span>