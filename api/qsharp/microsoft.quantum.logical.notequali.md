---
uid: Microsoft.Quantum.Logical.NotEqualI
title: De functie NotEqualI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualI
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 68e0e105a6b3742ec11e80ff92c39578a786aa85
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701408"
---
# <a name="notequali-function"></a><span data-ttu-id="5fc93-102">De functie NotEqualI</span><span class="sxs-lookup"><span data-stu-id="5fc93-102">NotEqualI function</span></span>

<span data-ttu-id="5fc93-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="5fc93-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="5fc93-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5fc93-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5fc93-105">Retourneert waar als en alleen als twee invoer waarden niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="5fc93-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="5fc93-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5fc93-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="5fc93-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5fc93-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5fc93-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="5fc93-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="5fc93-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="5fc93-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="5fc93-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="5fc93-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="5fc93-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5fc93-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5fc93-112">`true` Als en alleen als `a` is niet gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="5fc93-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fc93-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="5fc93-113">Remarks</span></span>

<span data-ttu-id="5fc93-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="5fc93-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualI(a, b);
```