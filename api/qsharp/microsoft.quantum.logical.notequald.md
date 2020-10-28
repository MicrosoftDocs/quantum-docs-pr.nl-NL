---
uid: Microsoft.Quantum.Logical.NotEqualD
title: De functie NotEqualD
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualD
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: dd21fcc1d0d73bd210303bfbf4f336386b912107
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708425"
---
# <a name="notequald-function"></a><span data-ttu-id="f9ee6-102">De functie NotEqualD</span><span class="sxs-lookup"><span data-stu-id="f9ee6-102">NotEqualD function</span></span>

<span data-ttu-id="f9ee6-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="f9ee6-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="f9ee6-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f9ee6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f9ee6-105">Retourneert waar als en alleen als twee invoer waarden niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="f9ee6-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="f9ee6-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f9ee6-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="f9ee6-107">a: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f9ee6-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f9ee6-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="f9ee6-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="f9ee6-109">b: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f9ee6-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f9ee6-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="f9ee6-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f9ee6-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f9ee6-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f9ee6-112">`true` Als en alleen als `a` is niet gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="f9ee6-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9ee6-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="f9ee6-113">Remarks</span></span>

<span data-ttu-id="f9ee6-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="f9ee6-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualD(a, b);
```