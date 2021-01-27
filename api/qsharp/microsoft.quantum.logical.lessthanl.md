---
uid: Microsoft.Quantum.Logical.LessThanL
title: De functie LessThanL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanL
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: d5753f9e1447fc1bd433703037fe44c86aaa659c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849152"
---
# <a name="lessthanl-function"></a><span data-ttu-id="70ce6-102">De functie LessThanL</span><span class="sxs-lookup"><span data-stu-id="70ce6-102">LessThanL function</span></span>

<span data-ttu-id="70ce6-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="70ce6-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="70ce6-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="70ce6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="70ce6-105">Retourneert waar als en alleen als een getal kleiner is dan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="70ce6-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="70ce6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="70ce6-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="70ce6-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="70ce6-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="70ce6-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="70ce6-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="70ce6-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="70ce6-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="70ce6-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="70ce6-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="70ce6-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="70ce6-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="70ce6-112">`true` Als en alleen als dit `a` strikt kleiner is dan `b` .</span><span class="sxs-lookup"><span data-stu-id="70ce6-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="70ce6-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="70ce6-113">Remarks</span></span>

<span data-ttu-id="70ce6-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="70ce6-114">The following are equivalent:</span></span>

```qsharp
let cond = a < b;
let cond = LessThanL(a, b);
```