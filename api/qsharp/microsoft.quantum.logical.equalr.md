---
uid: Microsoft.Quantum.Logical.EqualR
title: Functie EQUAL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualR
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 5aaa17303d75b27c3ac82cbe7d739a60016fdcb1
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701493"
---
# <a name="equalr-function"></a><span data-ttu-id="310dd-102">Functie EQUAL</span><span class="sxs-lookup"><span data-stu-id="310dd-102">EqualR function</span></span>

<span data-ttu-id="310dd-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="310dd-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="310dd-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="310dd-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="310dd-105">Retourneert waar als en alleen als twee invoer waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="310dd-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualR (a : Result, b : Result) : Bool
```


## <a name="input"></a><span data-ttu-id="310dd-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="310dd-106">Input</span></span>

### <a name="a--__invalidresult__"></a><span data-ttu-id="310dd-107">a: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="310dd-107">a : __invalid<Result>__</span></span>

<span data-ttu-id="310dd-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="310dd-108">The first value to be compared.</span></span>


### <a name="b--__invalidresult__"></a><span data-ttu-id="310dd-109">b: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="310dd-109">b : __invalid<Result>__</span></span>

<span data-ttu-id="310dd-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="310dd-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="310dd-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="310dd-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="310dd-112">`true` Als en alleen als `a` is gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="310dd-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="310dd-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="310dd-113">Remarks</span></span>

<span data-ttu-id="310dd-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="310dd-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualR(a, b);
```