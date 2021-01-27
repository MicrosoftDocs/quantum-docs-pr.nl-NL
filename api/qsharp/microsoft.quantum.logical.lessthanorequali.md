---
uid: Microsoft.Quantum.Logical.LessThanOrEqualI
title: De functie LessThanOrEqualI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualI
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 9438fc05b4ccb041b087f9cfeb30ac0c8cfcabd6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815611"
---
# <a name="lessthanorequali-function"></a><span data-ttu-id="88aac-102">De functie LessThanOrEqualI</span><span class="sxs-lookup"><span data-stu-id="88aac-102">LessThanOrEqualI function</span></span>

<span data-ttu-id="88aac-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="88aac-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="88aac-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="88aac-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="88aac-105">Retourneert waar als en alleen als een getal kleiner is dan of gelijk is aan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="88aac-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="88aac-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="88aac-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="88aac-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="88aac-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="88aac-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="88aac-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="88aac-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="88aac-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="88aac-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="88aac-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="88aac-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="88aac-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="88aac-112">`true` Als en alleen als deze `a` kleiner is dan of gelijk is aan `b` .</span><span class="sxs-lookup"><span data-stu-id="88aac-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="88aac-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="88aac-113">Remarks</span></span>

<span data-ttu-id="88aac-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="88aac-114">The following are equivalent:</span></span>

```qsharp
let cond = a <= b;
let cond = LessThanOrEqualI(a, b);
```