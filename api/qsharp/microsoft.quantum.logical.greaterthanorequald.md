---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualD
title: De functie GreaterThanOrEqualD
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualD
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: 98fa55c249f2ade414254d1bccda46a8602b828c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815869"
---
# <a name="greaterthanorequald-function"></a><span data-ttu-id="ea21c-102">De functie GreaterThanOrEqualD</span><span class="sxs-lookup"><span data-stu-id="ea21c-102">GreaterThanOrEqualD function</span></span>

<span data-ttu-id="ea21c-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="ea21c-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="ea21c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ea21c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ea21c-105">Retourneert waar als en alleen als een getal groter is dan of gelijk is aan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="ea21c-105">Returns true if and only if a number is greater than or equal to another number.</span></span>

```qsharp
function GreaterThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="ea21c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ea21c-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="ea21c-107">a: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ea21c-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ea21c-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="ea21c-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="ea21c-109">b: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ea21c-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ea21c-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="ea21c-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="ea21c-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ea21c-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ea21c-112">`true` Als en alleen als dit `a` groter is dan of gelijk is aan `b` .</span><span class="sxs-lookup"><span data-stu-id="ea21c-112">`true` if and only if `a` is greater than or is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea21c-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="ea21c-113">Remarks</span></span>

<span data-ttu-id="ea21c-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="ea21c-114">The following are equivalent:</span></span>

```qsharp
let cond = a >= b;
let cond = GreaterThanOrEqualD(a, b);
```