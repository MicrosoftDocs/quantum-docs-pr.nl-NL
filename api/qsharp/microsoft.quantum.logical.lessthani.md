---
uid: Microsoft.Quantum.Logical.LessThanI
title: De functie LessThanI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanI
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 204e62a87d2b3d0070946985030d038ead686457
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708430"
---
# <a name="lessthani-function"></a><span data-ttu-id="7a06c-102">De functie LessThanI</span><span class="sxs-lookup"><span data-stu-id="7a06c-102">LessThanI function</span></span>

<span data-ttu-id="7a06c-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="7a06c-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="7a06c-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7a06c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="7a06c-105">Retourneert waar als en alleen als een getal kleiner is dan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="7a06c-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="7a06c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="7a06c-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="7a06c-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7a06c-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7a06c-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="7a06c-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="7a06c-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="7a06c-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="7a06c-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="7a06c-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="7a06c-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="7a06c-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7a06c-112">`true` Als en alleen als dit `a` strikt kleiner is dan `b` .</span><span class="sxs-lookup"><span data-stu-id="7a06c-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a06c-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="7a06c-113">Remarks</span></span>

<span data-ttu-id="7a06c-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="7a06c-114">The following are equivalent:</span></span>

```Q#
let cond = a < b;
let cond = LessThanI(a, b);
```