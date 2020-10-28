---
uid: Microsoft.Quantum.Logical.GreaterThanD
title: De functie GreaterThanD
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanD
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 20414e80e08993a18331a8f0b385a1e4cc1255b3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701481"
---
# <a name="greaterthand-function"></a><span data-ttu-id="e4711-102">De functie GreaterThanD</span><span class="sxs-lookup"><span data-stu-id="e4711-102">GreaterThanD function</span></span>

<span data-ttu-id="e4711-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="e4711-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="e4711-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e4711-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e4711-105">Retourneert waar als en alleen als een getal groter is dan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="e4711-105">Returns true if and only if a number is greater than another number.</span></span>

```qsharp
function GreaterThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="e4711-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e4711-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="e4711-107">a: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e4711-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e4711-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="e4711-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="e4711-109">b: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e4711-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e4711-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="e4711-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="e4711-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e4711-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e4711-112">`true` Als en alleen als dit `a` strikt groter is dan `b` .</span><span class="sxs-lookup"><span data-stu-id="e4711-112">`true` if and only if `a` is strictly greater than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4711-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="e4711-113">Remarks</span></span>

<span data-ttu-id="e4711-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="e4711-114">The following are equivalent:</span></span>

```Q#
let cond = a > b;
let cond = GreaterThanD(a, b);
```