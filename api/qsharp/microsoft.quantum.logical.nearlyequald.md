---
uid: Microsoft.Quantum.Logical.NearlyEqualD
title: De functie NearlyEqualD
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NearlyEqualD
qsharp.summary: Returns true if and only if two inputs are nearly equal (that is, within a tolerance of 1e-12).
ms.openlocfilehash: 332f9ea1753b539eba7b931d5b948b2a238d1abf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701426"
---
# <a name="nearlyequald-function"></a><span data-ttu-id="2dc1e-102">De functie NearlyEqualD</span><span class="sxs-lookup"><span data-stu-id="2dc1e-102">NearlyEqualD function</span></span>

<span data-ttu-id="2dc1e-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="2dc1e-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="2dc1e-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2dc1e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2dc1e-105">Retourneert waar als en alleen als twee invoer bijna gelijk is (dat wil zeggen, binnen een tolerantie van 1e-12).</span><span class="sxs-lookup"><span data-stu-id="2dc1e-105">Returns true if and only if two inputs are nearly equal (that is, within a tolerance of 1e-12).</span></span>

```qsharp
function NearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="2dc1e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="2dc1e-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="2dc1e-107">a: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2dc1e-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2dc1e-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="2dc1e-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="2dc1e-109">b: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2dc1e-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2dc1e-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="2dc1e-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="2dc1e-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2dc1e-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2dc1e-112">`true` Als en alleen als `a` bijna gelijk is aan `b` .</span><span class="sxs-lookup"><span data-stu-id="2dc1e-112">`true` if and only if `a` is nearly equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2dc1e-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="2dc1e-113">Remarks</span></span>

<span data-ttu-id="2dc1e-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="2dc1e-114">The following are equivalent:</span></span>

```Q#
let cond = Microsoft.Quantum.Math.AbsD(a - b) < 1e-12;
let cond = NearlyEqualD(a, b);
```