---
uid: Microsoft.Quantum.Logical.EqualI
title: De functie EqualI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualI
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 6b805e76217e033cb0135cf85bd8f37a3eb8636a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701504"
---
# <a name="equali-function"></a><span data-ttu-id="869de-102">De functie EqualI</span><span class="sxs-lookup"><span data-stu-id="869de-102">EqualI function</span></span>

<span data-ttu-id="869de-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="869de-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="869de-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="869de-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="869de-105">Retourneert waar als en alleen als twee invoer waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="869de-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="869de-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="869de-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="869de-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="869de-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="869de-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="869de-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="869de-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="869de-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="869de-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="869de-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="869de-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="869de-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="869de-112">`true` Als en alleen als `a` is gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="869de-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="869de-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="869de-113">Remarks</span></span>

<span data-ttu-id="869de-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="869de-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualI(a, b);
```