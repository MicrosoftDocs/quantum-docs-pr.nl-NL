---
uid: Microsoft.Quantum.Logical.GreaterThanI
title: De functie GreaterThanI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanI
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 06cae04150f9f0164b06a4e3d4bb78242b41dc0b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197990"
---
# <a name="greaterthani-function"></a><span data-ttu-id="90ded-102">De functie GreaterThanI</span><span class="sxs-lookup"><span data-stu-id="90ded-102">GreaterThanI function</span></span>

<span data-ttu-id="90ded-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="90ded-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="90ded-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="90ded-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="90ded-105">Retourneert waar als en alleen als een getal groter is dan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="90ded-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="90ded-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="90ded-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="90ded-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="90ded-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="90ded-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="90ded-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="90ded-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="90ded-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="90ded-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="90ded-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="90ded-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="90ded-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="90ded-112">`true` Als en alleen als dit `a` strikt groter is dan `b` .</span><span class="sxs-lookup"><span data-stu-id="90ded-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="90ded-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="90ded-113">Remarks</span></span>

<span data-ttu-id="90ded-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="90ded-114">The following are equivalent:</span></span>

```Q#
let cond = a > b;
let cond = GreaterThanI(a, b);
```