---
uid: Microsoft.Quantum.Logical.GreaterThanL
title: De functie GreaterThanL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanL
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 676defa7824e53578504c559c6d8f24b2ffc1a88
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702074"
---
# <a name="greaterthanl-function"></a><span data-ttu-id="3a81a-102">De functie GreaterThanL</span><span class="sxs-lookup"><span data-stu-id="3a81a-102">GreaterThanL function</span></span>

<span data-ttu-id="3a81a-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="3a81a-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="3a81a-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3a81a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3a81a-105">Retourneert waar als en alleen als een getal groter is dan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="3a81a-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="3a81a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="3a81a-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="3a81a-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="3a81a-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="3a81a-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="3a81a-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="3a81a-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="3a81a-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="3a81a-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="3a81a-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="3a81a-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3a81a-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3a81a-112">`true` Als en alleen als dit `a` strikt groter is dan `b` .</span><span class="sxs-lookup"><span data-stu-id="3a81a-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a81a-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="3a81a-113">Remarks</span></span>

<span data-ttu-id="3a81a-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="3a81a-114">The following are equivalent:</span></span>

```Q#
let cond = a > b;
let cond = GreaterThanL(a, b);
```