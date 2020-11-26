---
uid: Microsoft.Quantum.Logical.GreaterThanL
title: De functie GreaterThanL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanL
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 5e1b2adab36b7937c83ea912b8a9cb148b626ee5
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197973"
---
# <a name="greaterthanl-function"></a><span data-ttu-id="d1579-102">De functie GreaterThanL</span><span class="sxs-lookup"><span data-stu-id="d1579-102">GreaterThanL function</span></span>

<span data-ttu-id="d1579-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="d1579-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="d1579-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d1579-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d1579-105">Retourneert waar als en alleen als een getal groter is dan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="d1579-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="d1579-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d1579-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="d1579-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d1579-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d1579-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="d1579-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="d1579-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="d1579-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="d1579-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="d1579-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="d1579-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d1579-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d1579-112">`true` Als en alleen als dit `a` strikt groter is dan `b` .</span><span class="sxs-lookup"><span data-stu-id="d1579-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1579-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d1579-113">Remarks</span></span>

<span data-ttu-id="d1579-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="d1579-114">The following are equivalent:</span></span>

```Q#
let cond = a > b;
let cond = GreaterThanL(a, b);
```