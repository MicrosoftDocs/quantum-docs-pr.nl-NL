---
uid: Microsoft.Quantum.Logical.NotEqualR
title: De functie NotEqualR
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualR
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 39601396a75d8c1b9193d4b8f34fa05466beff06
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848503"
---
# <a name="notequalr-function"></a><span data-ttu-id="d30a6-102">De functie NotEqualR</span><span class="sxs-lookup"><span data-stu-id="d30a6-102">NotEqualR function</span></span>

<span data-ttu-id="d30a6-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="d30a6-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="d30a6-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d30a6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d30a6-105">Retourneert waar als en alleen als twee invoer waarden niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="d30a6-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="d30a6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d30a6-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="d30a6-107">a: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="d30a6-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="d30a6-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="d30a6-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="d30a6-109">b: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="d30a6-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="d30a6-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="d30a6-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="d30a6-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d30a6-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d30a6-112">`true` Als en alleen als `a` is niet gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="d30a6-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="d30a6-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d30a6-113">Remarks</span></span>

<span data-ttu-id="d30a6-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="d30a6-114">The following are equivalent:</span></span>

```qsharp
let cond = a != b;
let cond = NotEqualR(a, b);
```