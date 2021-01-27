---
uid: Microsoft.Quantum.Logical.NearlyEqualD
title: De functie NearlyEqualD
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NearlyEqualD
qsharp.summary: Returns true if and only if two inputs are nearly equal (that is, within a tolerance of 1e-12).
ms.openlocfilehash: fbbf1f7a59600ecc4a0a59d1c08cd0e1310d2d20
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814375"
---
# <a name="nearlyequald-function"></a><span data-ttu-id="71919-102">De functie NearlyEqualD</span><span class="sxs-lookup"><span data-stu-id="71919-102">NearlyEqualD function</span></span>

<span data-ttu-id="71919-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="71919-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="71919-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="71919-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="71919-105">Retourneert waar als en alleen als twee invoer bijna gelijk is (dat wil zeggen, binnen een tolerantie van 1e-12).</span><span class="sxs-lookup"><span data-stu-id="71919-105">Returns true if and only if two inputs are nearly equal (that is, within a tolerance of 1e-12).</span></span>

```qsharp
function NearlyEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="71919-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="71919-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="71919-107">a: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="71919-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="71919-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="71919-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="71919-109">b: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="71919-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="71919-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="71919-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="71919-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="71919-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="71919-112">`true` Als en alleen als `a` bijna gelijk is aan `b` .</span><span class="sxs-lookup"><span data-stu-id="71919-112">`true` if and only if `a` is nearly equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="71919-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="71919-113">Remarks</span></span>

<span data-ttu-id="71919-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="71919-114">The following are equivalent:</span></span>

```qsharp
let cond = Microsoft.Quantum.Math.AbsD(a - b) < 1e-12;
let cond = NearlyEqualD(a, b);
```