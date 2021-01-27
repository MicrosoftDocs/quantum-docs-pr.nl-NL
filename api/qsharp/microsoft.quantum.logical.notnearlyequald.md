---
uid: Microsoft.Quantum.Logical.NotNearlyEqualD
title: De functie NotNearlyEqualD
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotNearlyEqualD
qsharp.summary: Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).
ms.openlocfilehash: 6e4cf3ec009f55ecc6345453c080520a3af6a8ef
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848491"
---
# <a name="notnearlyequald-function"></a><span data-ttu-id="b49e5-102">De functie NotNearlyEqualD</span><span class="sxs-lookup"><span data-stu-id="b49e5-102">NotNearlyEqualD function</span></span>

<span data-ttu-id="b49e5-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="b49e5-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="b49e5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b49e5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b49e5-105">Retourneert waar als twee invoer waarden niet bijna gelijk zijn (dat wil zeggen, niet binnen een tolerantie van 1e-12).</span><span class="sxs-lookup"><span data-stu-id="b49e5-105">Returns true if and only if two inputs are not nearly equal (that is, are not within a tolerance of 1e-12).</span></span>

```qsharp
function NotNearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="b49e5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b49e5-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="b49e5-107">a: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b49e5-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b49e5-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="b49e5-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="b49e5-109">b: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="b49e5-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="b49e5-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="b49e5-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="b49e5-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="b49e5-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="b49e5-112">`true` Als en alleen als `a` dat niet bijna gelijk is aan `b` .</span><span class="sxs-lookup"><span data-stu-id="b49e5-112">`true` if and only if `a` is not nearly equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="b49e5-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="b49e5-113">Remarks</span></span>

<span data-ttu-id="b49e5-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="b49e5-114">The following are equivalent:</span></span>

```qsharp
let cond = Microsoft.Quantum.Math.AbsD(a - b) >= 1e-12;
let cond = NotNearlyEqualD(a, b);
```