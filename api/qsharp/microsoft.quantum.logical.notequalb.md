---
uid: Microsoft.Quantum.Logical.NotEqualB
title: De functie NotEqualB
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualB
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: d5a9819bf3baa7c914487277fef308abbc8d25bd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701409"
---
# <a name="notequalb-function"></a><span data-ttu-id="e59b5-102">De functie NotEqualB</span><span class="sxs-lookup"><span data-stu-id="e59b5-102">NotEqualB function</span></span>

<span data-ttu-id="e59b5-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="e59b5-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="e59b5-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e59b5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e59b5-105">Retourneert waar als en alleen als twee invoer waarden niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="e59b5-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="e59b5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e59b5-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="e59b5-107">a: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e59b5-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e59b5-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="e59b5-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="e59b5-109">b: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e59b5-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e59b5-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="e59b5-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="e59b5-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="e59b5-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="e59b5-112">`true` Als en alleen als `a` is niet gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="e59b5-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="e59b5-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="e59b5-113">Remarks</span></span>

<span data-ttu-id="e59b5-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="e59b5-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualB(a, b);
```