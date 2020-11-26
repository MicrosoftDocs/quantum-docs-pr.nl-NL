---
uid: Microsoft.Quantum.Logical.EqualR
title: Functie EQUAL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualR
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: d68b2f1a26bf318400d3c88b37d9aabcc38cbdfe
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198003"
---
# <a name="equalr-function"></a><span data-ttu-id="145c5-102">Functie EQUAL</span><span class="sxs-lookup"><span data-stu-id="145c5-102">EqualR function</span></span>

<span data-ttu-id="145c5-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="145c5-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="145c5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="145c5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="145c5-105">Retourneert waar als en alleen als twee invoer waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="145c5-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="145c5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="145c5-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="145c5-107">a: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="145c5-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="145c5-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="145c5-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="145c5-109">b: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="145c5-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="145c5-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="145c5-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="145c5-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="145c5-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="145c5-112">`true` Als en alleen als `a` is gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="145c5-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="145c5-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="145c5-113">Remarks</span></span>

<span data-ttu-id="145c5-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="145c5-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualR(a, b);
```