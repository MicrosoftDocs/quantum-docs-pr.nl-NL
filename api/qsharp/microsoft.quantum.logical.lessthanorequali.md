---
uid: Microsoft.Quantum.Logical.LessThanOrEqualI
title: De functie LessThanOrEqualI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualI
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: dd934fde3fae9c1a43032b4b08ac03afa72798d1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701451"
---
# <a name="lessthanorequali-function"></a><span data-ttu-id="83891-102">De functie LessThanOrEqualI</span><span class="sxs-lookup"><span data-stu-id="83891-102">LessThanOrEqualI function</span></span>

<span data-ttu-id="83891-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="83891-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="83891-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="83891-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="83891-105">Retourneert waar als en alleen als een getal kleiner is dan of gelijk is aan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="83891-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="83891-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="83891-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="83891-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="83891-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="83891-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="83891-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="83891-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="83891-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="83891-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="83891-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="83891-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="83891-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="83891-112">`true` Als en alleen als deze `a` kleiner is dan of gelijk is aan `b` .</span><span class="sxs-lookup"><span data-stu-id="83891-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="83891-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="83891-113">Remarks</span></span>

<span data-ttu-id="83891-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="83891-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualI(a, b);
```