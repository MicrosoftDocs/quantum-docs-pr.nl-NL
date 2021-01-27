---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualL
title: De functie GreaterThanOrEqualL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualL
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: f33a7f17f3391d87e3eff9fb31939586036e83f8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815851"
---
# <a name="greaterthanorequall-function"></a><span data-ttu-id="51fbf-102">De functie GreaterThanOrEqualL</span><span class="sxs-lookup"><span data-stu-id="51fbf-102">GreaterThanOrEqualL function</span></span>

<span data-ttu-id="51fbf-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="51fbf-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="51fbf-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="51fbf-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="51fbf-105">Retourneert waar als en alleen als een getal groter is dan of gelijk is aan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="51fbf-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="51fbf-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="51fbf-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="51fbf-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="51fbf-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="51fbf-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="51fbf-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="51fbf-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="51fbf-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="51fbf-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="51fbf-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="51fbf-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="51fbf-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="51fbf-112">`true` Als en alleen als dit `a` groter is dan of gelijk is aan `b` .</span><span class="sxs-lookup"><span data-stu-id="51fbf-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="51fbf-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="51fbf-113">Remarks</span></span>

<span data-ttu-id="51fbf-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="51fbf-114">The following are equivalent:</span></span>

```qsharp
let cond = a >= b;
let cond = GreaterThanOrEqualL(a, b);
```