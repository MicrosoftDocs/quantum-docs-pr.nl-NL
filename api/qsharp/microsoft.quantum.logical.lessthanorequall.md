---
uid: Microsoft.Quantum.Logical.LessThanOrEqualL
title: De functie LessThanOrEqualL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualL
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 333b76fc4885104e107dd25003a4e0dd5a9dd4af
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701445"
---
# <a name="lessthanorequall-function"></a><span data-ttu-id="b4a51-102">De functie LessThanOrEqualL</span><span class="sxs-lookup"><span data-stu-id="b4a51-102">LessThanOrEqualL function</span></span>

<span data-ttu-id="b4a51-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="b4a51-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="b4a51-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b4a51-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b4a51-105">Retourneert waar als en alleen als een getal kleiner is dan of gelijk is aan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="b4a51-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="b4a51-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b4a51-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="b4a51-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b4a51-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="b4a51-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="b4a51-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="b4a51-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="b4a51-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="b4a51-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="b4a51-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="b4a51-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b4a51-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="b4a51-112">`true` Als en alleen als deze `a` kleiner is dan of gelijk is aan `b` .</span><span class="sxs-lookup"><span data-stu-id="b4a51-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4a51-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="b4a51-113">Remarks</span></span>

<span data-ttu-id="b4a51-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="b4a51-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualL(a, b);
```