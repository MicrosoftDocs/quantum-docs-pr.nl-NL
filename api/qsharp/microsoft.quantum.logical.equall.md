---
uid: Microsoft.Quantum.Logical.EqualL
title: De functie EQUAL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualL
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 395b8fedd3b3334939c2a4b5602ee19e0c6e34b0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198109"
---
# <a name="equall-function"></a><span data-ttu-id="a9e01-102">De functie EQUAL</span><span class="sxs-lookup"><span data-stu-id="a9e01-102">EqualL function</span></span>

<span data-ttu-id="a9e01-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="a9e01-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="a9e01-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a9e01-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a9e01-105">Retourneert waar als en alleen als twee invoer waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="a9e01-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="a9e01-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a9e01-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="a9e01-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a9e01-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="a9e01-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="a9e01-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="a9e01-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="a9e01-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="a9e01-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="a9e01-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a9e01-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a9e01-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a9e01-112">`true` Als en alleen als `a` is gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="a9e01-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9e01-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="a9e01-113">Remarks</span></span>

<span data-ttu-id="a9e01-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="a9e01-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualL(a, b);
```