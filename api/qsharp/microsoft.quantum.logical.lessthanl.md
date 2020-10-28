---
uid: Microsoft.Quantum.Logical.LessThanL
title: De functie LessThanL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanL
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: fde57bcd9960056461bddac54300c298def8f7d5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701462"
---
# <a name="lessthanl-function"></a><span data-ttu-id="593a8-102">De functie LessThanL</span><span class="sxs-lookup"><span data-stu-id="593a8-102">LessThanL function</span></span>

<span data-ttu-id="593a8-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="593a8-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="593a8-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="593a8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="593a8-105">Retourneert waar als en alleen als een getal kleiner is dan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="593a8-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="593a8-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="593a8-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="593a8-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="593a8-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="593a8-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="593a8-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="593a8-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="593a8-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="593a8-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="593a8-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="593a8-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="593a8-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="593a8-112">`true` Als en alleen als dit `a` strikt kleiner is dan `b` .</span><span class="sxs-lookup"><span data-stu-id="593a8-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="593a8-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="593a8-113">Remarks</span></span>

<span data-ttu-id="593a8-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="593a8-114">The following are equivalent:</span></span>

```Q#
let cond = a < b;
let cond = LessThanL(a, b);
```