---
uid: Microsoft.Quantum.Logical.NotNearlyEqualD
title: De functie NotNearlyEqualD
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotNearlyEqualD
qsharp.summary: Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).
ms.openlocfilehash: d9e4cc5b0cfba3989ae64e494d0daa52069718a4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707013"
---
# <a name="notnearlyequald-function"></a><span data-ttu-id="dedae-102">De functie NotNearlyEqualD</span><span class="sxs-lookup"><span data-stu-id="dedae-102">NotNearlyEqualD function</span></span>

<span data-ttu-id="dedae-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="dedae-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="dedae-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dedae-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dedae-105">Retourneert waar als twee invoer waarden niet bijna gelijk zijn (dat wil zeggen, niet binnen een tolerantie van 1e-12).</span><span class="sxs-lookup"><span data-stu-id="dedae-105">Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).</span></span>

```qsharp
function NotNearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="dedae-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="dedae-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="dedae-107">a: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="dedae-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="dedae-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="dedae-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="dedae-109">b: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="dedae-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="dedae-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="dedae-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="dedae-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="dedae-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="dedae-112">`true` Als en alleen als `a` dat niet bijna gelijk is aan `b` .</span><span class="sxs-lookup"><span data-stu-id="dedae-112">`true` if and only if `a` is not nearly equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="dedae-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="dedae-113">Remarks</span></span>

<span data-ttu-id="dedae-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="dedae-114">The following are equivalent:</span></span>

```Q#
let cond = Microsoft.Quantum.Math.AbsD(a - b) >= 1e-12;
let cond = NotNearlyEqualD(a, b);
```