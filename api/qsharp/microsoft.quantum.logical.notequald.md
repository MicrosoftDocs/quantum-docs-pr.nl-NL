---
uid: Microsoft.Quantum.Logical.NotEqualD
title: De functie NotEqualD
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualD
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 38f30309a4c27a5ef7e112a09a0efe3b5512d4e3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849055"
---
# <a name="notequald-function"></a><span data-ttu-id="e3a36-102">De functie NotEqualD</span><span class="sxs-lookup"><span data-stu-id="e3a36-102">NotEqualD function</span></span>

<span data-ttu-id="e3a36-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="e3a36-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="e3a36-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e3a36-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e3a36-105">Retourneert waar als en alleen als twee invoer waarden niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="e3a36-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="e3a36-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e3a36-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="e3a36-107">a: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e3a36-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e3a36-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="e3a36-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="e3a36-109">b: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e3a36-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e3a36-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="e3a36-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="e3a36-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e3a36-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e3a36-112">`true` Als en alleen als `a` is niet gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="e3a36-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a36-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="e3a36-113">Remarks</span></span>

<span data-ttu-id="e3a36-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="e3a36-114">The following are equivalent:</span></span>

```qsharp
let cond = a != b;
let cond = NotEqualD(a, b);
```