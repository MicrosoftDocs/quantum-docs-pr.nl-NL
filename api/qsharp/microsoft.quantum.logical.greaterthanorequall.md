---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualL
title: De functie GreaterThanOrEqualL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualL
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 5536c009d6e78eac9ab2320b42aec7d2d82946eb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197752"
---
# <a name="greaterthanorequall-function"></a><span data-ttu-id="1d612-102">De functie GreaterThanOrEqualL</span><span class="sxs-lookup"><span data-stu-id="1d612-102">GreaterThanOrEqualL function</span></span>

<span data-ttu-id="1d612-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="1d612-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="1d612-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1d612-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1d612-105">Retourneert waar als en alleen als een getal groter is dan of gelijk is aan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="1d612-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="1d612-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="1d612-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="1d612-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1d612-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="1d612-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="1d612-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="1d612-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="1d612-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="1d612-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="1d612-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="1d612-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="1d612-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="1d612-112">`true` Als en alleen als dit `a` groter is dan of gelijk is aan `b` .</span><span class="sxs-lookup"><span data-stu-id="1d612-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d612-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="1d612-113">Remarks</span></span>

<span data-ttu-id="1d612-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="1d612-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualL(a, b);
```