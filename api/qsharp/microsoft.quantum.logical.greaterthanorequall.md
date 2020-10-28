---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualL
title: De functie GreaterThanOrEqualL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualL
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: a59a9eca2941a44a70ec5a379b146ac459390bd4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708070"
---
# <a name="greaterthanorequall-function"></a><span data-ttu-id="f4be6-102">De functie GreaterThanOrEqualL</span><span class="sxs-lookup"><span data-stu-id="f4be6-102">GreaterThanOrEqualL function</span></span>

<span data-ttu-id="f4be6-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="f4be6-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="f4be6-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f4be6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f4be6-105">Retourneert waar als en alleen als een getal groter is dan of gelijk is aan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="f4be6-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="f4be6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f4be6-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="f4be6-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="f4be6-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="f4be6-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="f4be6-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="f4be6-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="f4be6-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="f4be6-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="f4be6-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f4be6-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f4be6-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f4be6-112">`true` Als en alleen als dit `a` groter is dan of gelijk is aan `b` .</span><span class="sxs-lookup"><span data-stu-id="f4be6-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4be6-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="f4be6-113">Remarks</span></span>

<span data-ttu-id="f4be6-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="f4be6-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualL(a, b);
```