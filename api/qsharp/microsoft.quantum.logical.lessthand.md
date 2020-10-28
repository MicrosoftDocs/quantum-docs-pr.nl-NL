---
uid: Microsoft.Quantum.Logical.LessThanD
title: De functie LessThanD
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanD
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 8cd274d5e299df2f556006baf7457d54aebcd071
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708431"
---
# <a name="lessthand-function"></a><span data-ttu-id="40168-102">De functie LessThanD</span><span class="sxs-lookup"><span data-stu-id="40168-102">LessThanD function</span></span>

<span data-ttu-id="40168-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="40168-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="40168-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="40168-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="40168-105">Retourneert waar als en alleen als een getal kleiner is dan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="40168-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="40168-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="40168-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="40168-107">a: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="40168-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="40168-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="40168-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="40168-109">b: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="40168-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="40168-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="40168-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="40168-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="40168-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="40168-112">`true` Als en alleen als dit `a` strikt kleiner is dan `b` .</span><span class="sxs-lookup"><span data-stu-id="40168-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="40168-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="40168-113">Remarks</span></span>

<span data-ttu-id="40168-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="40168-114">The following are equivalent:</span></span>

```Q#
let cond = a < b;
let cond = LessThanD(a, b);
```