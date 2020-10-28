---
uid: Microsoft.Quantum.Math.ExpModI
title: De functie ExpModI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModI
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: e31273702a9850d0162f160ca412ff6d50f38b28
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708377"
---
# <a name="expmodi-function"></a><span data-ttu-id="6d6e6-102">De functie ExpModI</span><span class="sxs-lookup"><span data-stu-id="6d6e6-102">ExpModI function</span></span>

<span data-ttu-id="6d6e6-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="6d6e6-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="6d6e6-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6d6e6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6d6e6-105">Retourneert een geheel getal dat tot een bepaalde macht is verheven, ten opzichte van een bepaalde modulus.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModI (expBase : Int, power : Int, modulus : Int) : Int
```


## <a name="description"></a><span data-ttu-id="6d6e6-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6d6e6-106">Description</span></span>

<span data-ttu-id="6d6e6-107">Laat ons expBase van $x $, kracht door $p $ en modulus door $N $.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="6d6e6-108">De functie retourneert $x ^ p \operatorname{mod} N $.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="6d6e6-109">We gaan ervan uit dat $N $, $x $ positief is en de stroom niet negatief is.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="6d6e6-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="6d6e6-110">Input</span></span>

### <a name="expbase--int"></a><span data-ttu-id="6d6e6-111">expBase: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6d6e6-111">expBase : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="power--int"></a><span data-ttu-id="6d6e6-112">energie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6d6e6-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="modulus--int"></a><span data-ttu-id="6d6e6-113">modulus: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6d6e6-113">modulus : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--int"></a><span data-ttu-id="6d6e6-114">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="6d6e6-114">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>



## <a name="remarks"></a><span data-ttu-id="6d6e6-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="6d6e6-115">Remarks</span></span>

<span data-ttu-id="6d6e6-116">Neemt de tijd in verhouding tot het aantal bits in `power` , niet de `power` zelf.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>