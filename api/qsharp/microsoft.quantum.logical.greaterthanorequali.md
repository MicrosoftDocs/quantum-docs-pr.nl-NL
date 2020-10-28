---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualI
title: De functie GreaterThanOrEqualI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualI
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 292599c18d2aac44cef8f0eecca38eb1fbe22061
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708436"
---
# <a name="greaterthanorequali-function"></a><span data-ttu-id="113d0-102">De functie GreaterThanOrEqualI</span><span class="sxs-lookup"><span data-stu-id="113d0-102">GreaterThanOrEqualI function</span></span>

<span data-ttu-id="113d0-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="113d0-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="113d0-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="113d0-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="113d0-105">Retourneert waar als en alleen als een getal groter is dan of gelijk is aan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="113d0-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="113d0-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="113d0-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="113d0-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="113d0-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="113d0-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="113d0-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="113d0-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="113d0-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="113d0-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="113d0-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="113d0-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="113d0-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="113d0-112">`true` Als en alleen als dit `a` groter is dan of gelijk is aan `b` .</span><span class="sxs-lookup"><span data-stu-id="113d0-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="113d0-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="113d0-113">Remarks</span></span>

<span data-ttu-id="113d0-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="113d0-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualI(a, b);
```