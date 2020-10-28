---
uid: Microsoft.Quantum.Logical.LessThanOrEqualD
title: De functie LessThanOrEqualD
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualD
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 7b0e9da379bd67eb78a80e7a535a15dcb8ba85c7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701457"
---
# <a name="lessthanorequald-function"></a><span data-ttu-id="91105-102">De functie LessThanOrEqualD</span><span class="sxs-lookup"><span data-stu-id="91105-102">LessThanOrEqualD function</span></span>

<span data-ttu-id="91105-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="91105-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="91105-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="91105-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="91105-105">Retourneert waar als en alleen als een getal kleiner is dan of gelijk is aan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="91105-105">Returns true if and only if a number is less than or equal to another number.</span></span>

```qsharp
function LessThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="91105-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="91105-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="91105-107">a: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="91105-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="91105-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="91105-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="91105-109">b: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="91105-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="91105-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="91105-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="91105-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="91105-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="91105-112">`true` Als en alleen als deze `a` kleiner is dan of gelijk is aan `b` .</span><span class="sxs-lookup"><span data-stu-id="91105-112">`true` if and only if `a` is less than or equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="91105-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="91105-113">Remarks</span></span>

<span data-ttu-id="91105-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="91105-114">The following are equivalent:</span></span>

```Q#
let cond = a <= b;
let cond = LessThanOrEqualD(a, b);
```