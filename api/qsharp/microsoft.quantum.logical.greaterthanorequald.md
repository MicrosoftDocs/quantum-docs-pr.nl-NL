---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualD
title: De functie GreaterThanOrEqualD
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualD
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 0c9fa353b549d3c137beac3bcc3cfb0e742f6d07
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197803"
---
# <a name="greaterthanorequald-function"></a><span data-ttu-id="af2e6-102">De functie GreaterThanOrEqualD</span><span class="sxs-lookup"><span data-stu-id="af2e6-102">GreaterThanOrEqualD function</span></span>

<span data-ttu-id="af2e6-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="af2e6-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="af2e6-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="af2e6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="af2e6-105">Retourneert waar als en alleen als een getal groter is dan of gelijk is aan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="af2e6-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="af2e6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="af2e6-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="af2e6-107">a: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="af2e6-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="af2e6-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="af2e6-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="af2e6-109">b: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="af2e6-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="af2e6-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="af2e6-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="af2e6-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="af2e6-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="af2e6-112">`true` Als en alleen als dit `a` groter is dan of gelijk is aan `b` .</span><span class="sxs-lookup"><span data-stu-id="af2e6-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="af2e6-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="af2e6-113">Remarks</span></span>

<span data-ttu-id="af2e6-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="af2e6-114">The following are equivalent:</span></span>

```Q#
let cond = a >= b;
let cond = GreaterThanOrEqualD(a, b);
```