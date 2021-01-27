---
uid: Microsoft.Quantum.Logical.LessThanD
title: De functie LessThanD
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanD
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 7135ed4b3414d143f5020496ae524bf89980a8a1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849161"
---
# <a name="lessthand-function"></a><span data-ttu-id="cc142-102">De functie LessThanD</span><span class="sxs-lookup"><span data-stu-id="cc142-102">LessThanD function</span></span>

<span data-ttu-id="cc142-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="cc142-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="cc142-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cc142-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cc142-105">Retourneert waar als en alleen als een getal kleiner is dan een ander getal.</span><span class="sxs-lookup"><span data-stu-id="cc142-105">Returns true if and only if a number is less than another number.</span></span>

```qsharp
function LessThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="cc142-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="cc142-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="cc142-107">a: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cc142-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="cc142-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="cc142-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="cc142-109">b: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="cc142-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="cc142-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="cc142-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="cc142-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="cc142-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="cc142-112">`true` Als en alleen als dit `a` strikt kleiner is dan `b` .</span><span class="sxs-lookup"><span data-stu-id="cc142-112">`true` if and only if `a` is strictly less than `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc142-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="cc142-113">Remarks</span></span>

<span data-ttu-id="cc142-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="cc142-114">The following are equivalent:</span></span>

```qsharp
let cond = a < b;
let cond = LessThanD(a, b);
```