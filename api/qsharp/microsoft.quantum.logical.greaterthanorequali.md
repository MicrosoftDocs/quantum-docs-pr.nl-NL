---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualI
title: De functie GreaterThanOrEqualI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualI
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: c1a513500c8a70bd7628976974387cba48162e80
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849187"
---
# <a name="greaterthanorequali-function"></a><span data-ttu-id="1593b-102">De functie GreaterThanOrEqualI</span><span class="sxs-lookup"><span data-stu-id="1593b-102">GreaterThanOrEqualI function</span></span>

<span data-ttu-id="1593b-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="1593b-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="1593b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1593b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1593b-105">Retourneert waar als en alleen als een getal groter is dan of gelijk is aan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="1593b-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="1593b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="1593b-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="1593b-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1593b-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1593b-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="1593b-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="1593b-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1593b-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1593b-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="1593b-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="1593b-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1593b-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="1593b-112">`true` Als en alleen als dit `a` groter is dan of gelijk is aan `b` .</span><span class="sxs-lookup"><span data-stu-id="1593b-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="1593b-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="1593b-113">Remarks</span></span>

<span data-ttu-id="1593b-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="1593b-114">The following are equivalent:</span></span>

```qsharp
let cond = a >= b;
let cond = GreaterThanOrEqualI(a, b);
```