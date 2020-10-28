---
uid: Microsoft.Quantum.Math.ExpModL
title: De functie ExpModL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Math
qsharp.name: ExpModL
qsharp.summary: Returns an integer raised to a given power, with respect to a given modulus.
ms.openlocfilehash: 73d434bd364847b4e5e06d1a9f460424e0c50850
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708533"
---
# <a name="expmodl-function"></a><span data-ttu-id="dd057-102">De functie ExpModL</span><span class="sxs-lookup"><span data-stu-id="dd057-102">ExpModL function</span></span>

<span data-ttu-id="dd057-103">Naam ruimte: [micro soft. Quantum. math](xref:Microsoft.Quantum.Math)</span><span class="sxs-lookup"><span data-stu-id="dd057-103">Namespace: [Microsoft.Quantum.Math](xref:Microsoft.Quantum.Math)</span></span>

<span data-ttu-id="dd057-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dd057-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dd057-105">Retourneert een geheel getal dat tot een bepaalde macht is verheven, ten opzichte van een bepaalde modulus.</span><span class="sxs-lookup"><span data-stu-id="dd057-105">Returns an integer raised to a given power, with respect to a given modulus.</span></span>

```qsharp
function ExpModL (expBase : BigInt, power : BigInt, modulus : BigInt) : BigInt
```


## <a name="description"></a><span data-ttu-id="dd057-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="dd057-106">Description</span></span>

<span data-ttu-id="dd057-107">Laat ons expBase van $x $, kracht door $p $ en modulus door $N $.</span><span class="sxs-lookup"><span data-stu-id="dd057-107">Let us denote expBase by $x$, power by $p$ and modulus by $N$.</span></span>
<span data-ttu-id="dd057-108">De functie retourneert $x ^ p \operatorname{mod} N $.</span><span class="sxs-lookup"><span data-stu-id="dd057-108">The function returns $x^p \operatorname{mod} N$.</span></span>

<span data-ttu-id="dd057-109">We gaan ervan uit dat $N $, $x $ positief is en de stroom niet negatief is.</span><span class="sxs-lookup"><span data-stu-id="dd057-109">We assume that $N$, $x$ are positive and power is non-negative.</span></span>

## <a name="input"></a><span data-ttu-id="dd057-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="dd057-110">Input</span></span>

### <a name="expbase--bigint"></a><span data-ttu-id="dd057-111">expBase: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="dd057-111">expBase : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="power--bigint"></a><span data-ttu-id="dd057-112">macht: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="dd057-112">power : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>




### <a name="modulus--bigint"></a><span data-ttu-id="dd057-113">modulus: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="dd057-113">modulus : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>





## <a name="output--bigint"></a><span data-ttu-id="dd057-114">Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="dd057-114">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>



## <a name="remarks"></a><span data-ttu-id="dd057-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="dd057-115">Remarks</span></span>

<span data-ttu-id="dd057-116">Neemt de tijd in verhouding tot het aantal bits in `power` , niet de `power` zelf.</span><span class="sxs-lookup"><span data-stu-id="dd057-116">Takes time proportional to the number of bits in `power`, not the `power` itself.</span></span>