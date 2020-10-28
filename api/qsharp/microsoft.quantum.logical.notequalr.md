---
uid: Microsoft.Quantum.Logical.NotEqualR
title: De functie NotEqualR
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 06615c7ffb6aafc296077990dfca0ce25e1e00fa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701391"
---
# <a name="notequalr-function"></a><span data-ttu-id="02294-102">De functie NotEqualR</span><span class="sxs-lookup"><span data-stu-id="02294-102">NotEqualR function</span></span>

<span data-ttu-id="02294-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="02294-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="02294-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="02294-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="02294-105">Retourneert waar als en alleen als twee invoer waarden niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="02294-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="02294-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="02294-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="02294-107">a: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="02294-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="02294-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="02294-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="02294-109">b: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="02294-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="02294-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="02294-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="02294-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="02294-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="02294-112">`true` Als en alleen als `a` is niet gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="02294-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="02294-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="02294-113">Remarks</span></span>

<span data-ttu-id="02294-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="02294-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualR(a, b);
```