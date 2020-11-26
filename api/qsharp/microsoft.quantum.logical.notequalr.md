---
uid: Microsoft.Quantum.Logical.NotEqualR
title: De functie NotEqualR
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 4ac6cf4b220fa42c8eb946d6fbcad4cdb191afcd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197191"
---
# <a name="notequalr-function"></a><span data-ttu-id="c4335-102">De functie NotEqualR</span><span class="sxs-lookup"><span data-stu-id="c4335-102">NotEqualR function</span></span>

<span data-ttu-id="c4335-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="c4335-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="c4335-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c4335-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c4335-105">Retourneert waar als en alleen als twee invoer waarden niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="c4335-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="c4335-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c4335-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="c4335-107">a: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="c4335-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="c4335-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="c4335-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="c4335-109">b: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="c4335-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="c4335-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="c4335-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="c4335-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c4335-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c4335-112">`true` Als en alleen als `a` is niet gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="c4335-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4335-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c4335-113">Remarks</span></span>

<span data-ttu-id="c4335-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="c4335-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualR(a, b);
```