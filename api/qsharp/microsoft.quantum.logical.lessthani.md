---
uid: Microsoft.Quantum.Logical.LessThanI
title: De functie LessThanI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanI
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 69c3d7c414967b830c15189c895a2b34f409c7b3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815836"
---
# <a name="lessthani-function"></a><span data-ttu-id="51d60-102">De functie LessThanI</span><span class="sxs-lookup"><span data-stu-id="51d60-102">LessThanI function</span></span>

<span data-ttu-id="51d60-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="51d60-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="51d60-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="51d60-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="51d60-105">Retourneert waar als en alleen als een getal kleiner is dan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="51d60-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="51d60-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="51d60-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="51d60-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="51d60-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="51d60-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="51d60-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="51d60-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="51d60-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="51d60-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="51d60-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="51d60-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="51d60-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="51d60-112">`true` Als en alleen als dit `a` strikt kleiner is dan `b` .</span><span class="sxs-lookup"><span data-stu-id="51d60-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="51d60-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="51d60-113">Remarks</span></span>

<span data-ttu-id="51d60-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="51d60-114">The following are equivalent:</span></span>

```qsharp
let cond = a < b;
let cond = LessThanI(a, b);
```