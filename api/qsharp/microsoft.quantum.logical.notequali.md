---
uid: Microsoft.Quantum.Logical.NotEqualI
title: De functie NotEqualI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualI
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: f88ae08f45c284f65151419c214705c74c3fadac
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814507"
---
# <a name="notequali-function"></a><span data-ttu-id="cba38-102">De functie NotEqualI</span><span class="sxs-lookup"><span data-stu-id="cba38-102">NotEqualI function</span></span>

<span data-ttu-id="cba38-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="cba38-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="cba38-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cba38-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cba38-105">Retourneert waar als en alleen als twee invoer waarden niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="cba38-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="cba38-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="cba38-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="cba38-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cba38-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cba38-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="cba38-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="cba38-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="cba38-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="cba38-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="cba38-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="cba38-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="cba38-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="cba38-112">`true` Als en alleen als `a` is niet gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="cba38-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="cba38-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="cba38-113">Remarks</span></span>

<span data-ttu-id="cba38-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="cba38-114">The following are equivalent:</span></span>

```qsharp
let cond = a != b;
let cond = NotEqualI(a, b);
```