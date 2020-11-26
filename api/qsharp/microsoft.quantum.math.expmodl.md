---
uid: Microsoft.Quantum.Math.ExpModL
title: De functie ExpModL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 07da113caeb9f6f3f3f3f92f13478f33021bfa14
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210741"
---
# <a name="expmodl-function"></a><span data-ttu-id="b010a-102">De functie ExpModL</span><span class="sxs-lookup"><span data-stu-id="b010a-102">ExpModL function</span></span>

<span data-ttu-id="b010a-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="b010a-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="b010a-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b010a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b010a-105">Retourneert een geheel getal dat tot een bepaalde macht is verheven, ten opzichte van een bepaalde modulus.</span><span class="sxs-lookup"><span data-stu-id="b010a-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModL (expBase : BigInt, power : BigInt, modulus : BigInt) : BigInt
```


## <a name="description"></a><span data-ttu-id="b010a-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="b010a-106">Description</span></span>

<span data-ttu-id="b010a-107">Laat ons expBase van $x $, kracht door $p $ en modulus door $N $.</span><span class="sxs-lookup"><span data-stu-id="b010a-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="b010a-108">De functie retourneert $x ^ p \operatorname{mod} N $.</span><span class="sxs-lookup"><span data-stu-id="b010a-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="b010a-109">We gaan ervan uit dat $N $, $x $ positief is en de stroom niet negatief is.</span><span class="sxs-lookup"><span data-stu-id="b010a-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="b010a-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="b010a-110">Input</span></span>

### <a name="expbase--bigint"></a><span data-ttu-id="b010a-111">expBase: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b010a-111">expBase : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="power--bigint"></a><span data-ttu-id="b010a-112">macht: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b010a-112">power : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="modulus--bigint"></a><span data-ttu-id="b010a-113">modulus: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b010a-113">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigint"></a><span data-ttu-id="b010a-114">Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b010a-114">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>



## <a name="remarks"></a><span data-ttu-id="b010a-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="b010a-115">Remarks</span></span>

<span data-ttu-id="b010a-116">Neemt de tijd in verhouding tot het aantal bits in `power` , niet de `power` zelf.</span><span class="sxs-lookup"><span data-stu-id="b010a-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>