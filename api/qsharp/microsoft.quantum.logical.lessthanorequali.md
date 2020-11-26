---
uid: Microsoft.Quantum.Logical.LessThanOrEqualI
title: De functie LessThanOrEqualI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualI
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: b2974c9bc84d0b4366767f47682ab542f85063e2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197563"
---
# <a name="lessthanorequali-function"></a><span data-ttu-id="1fc1e-102">De functie LessThanOrEqualI</span><span class="sxs-lookup"><span data-stu-id="1fc1e-102">LessThanOrEqualI function</span></span>

<span data-ttu-id="1fc1e-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="1fc1e-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="1fc1e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1fc1e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1fc1e-105">Retourneert waar als en alleen als een getal kleiner is dan of gelijk is aan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="1fc1e-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="1fc1e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="1fc1e-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="1fc1e-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1fc1e-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1fc1e-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="1fc1e-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="1fc1e-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="1fc1e-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="1fc1e-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="1fc1e-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="1fc1e-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1fc1e-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="1fc1e-112">`true` Als en alleen als deze `a` kleiner is dan of gelijk is aan `b` .</span><span class="sxs-lookup"><span data-stu-id="1fc1e-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fc1e-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="1fc1e-113">Remarks</span></span>

<span data-ttu-id="1fc1e-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="1fc1e-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualI(a, b);
```