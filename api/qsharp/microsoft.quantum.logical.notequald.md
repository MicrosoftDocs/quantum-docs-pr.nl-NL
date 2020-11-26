---
uid: Microsoft.Quantum.Logical.NotEqualD
title: De functie NotEqualD
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualD
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 4599d7125dbc67547af454183f620e8d84f2caf7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96197242"
---
# <a name="notequald-function"></a><span data-ttu-id="ba7ef-102">De functie NotEqualD</span><span class="sxs-lookup"><span data-stu-id="ba7ef-102">NotEqualD function</span></span>

<span data-ttu-id="ba7ef-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="ba7ef-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="ba7ef-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ba7ef-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ba7ef-105">Retourneert waar als en alleen als twee invoer waarden niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="ba7ef-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="ba7ef-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ba7ef-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="ba7ef-107">a: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ba7ef-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ba7ef-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="ba7ef-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="ba7ef-109">b: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ba7ef-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ba7ef-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="ba7ef-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="ba7ef-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ba7ef-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ba7ef-112">`true` Als en alleen als `a` is niet gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="ba7ef-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba7ef-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="ba7ef-113">Remarks</span></span>

<span data-ttu-id="ba7ef-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="ba7ef-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualD(a, b);
```