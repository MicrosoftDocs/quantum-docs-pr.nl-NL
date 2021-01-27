---
uid: Microsoft.Quantum.Logical.GreaterThanL
title: De functie GreaterThanL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanL
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 2247c1c1ae8b37b59e87c0c68b06fd1094c9003b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849205"
---
# <a name="greaterthanl-function"></a><span data-ttu-id="12c07-102">De functie GreaterThanL</span><span class="sxs-lookup"><span data-stu-id="12c07-102">GreaterThanL function</span></span>

<span data-ttu-id="12c07-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="12c07-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="12c07-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="12c07-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="12c07-105">Retourneert waar als en alleen als een getal groter is dan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="12c07-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="12c07-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="12c07-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="12c07-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="12c07-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="12c07-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="12c07-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="12c07-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="12c07-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="12c07-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="12c07-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="12c07-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="12c07-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="12c07-112">`true` Als en alleen als dit `a` strikt groter is dan `b` .</span><span class="sxs-lookup"><span data-stu-id="12c07-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="12c07-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="12c07-113">Remarks</span></span>

<span data-ttu-id="12c07-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="12c07-114">The following are equivalent:</span></span>

```qsharp
let cond = a > b;
let cond = GreaterThanL(a, b);
```