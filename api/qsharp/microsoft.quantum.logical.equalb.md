---
uid: Microsoft.Quantum.Logical.EqualB
title: De functie EqualB
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualB
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 91ab51180018a9b95a2f9010477c0a24f3a54617
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707052"
---
# <a name="equalb-function"></a><span data-ttu-id="9cc73-102">De functie EqualB</span><span class="sxs-lookup"><span data-stu-id="9cc73-102">EqualB function</span></span>

<span data-ttu-id="9cc73-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="9cc73-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="9cc73-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9cc73-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9cc73-105">Retourneert waar als en alleen als twee invoer waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="9cc73-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="9cc73-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9cc73-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="9cc73-107">a: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9cc73-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9cc73-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="9cc73-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="9cc73-109">b: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9cc73-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9cc73-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="9cc73-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="9cc73-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9cc73-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9cc73-112">`true` Als en alleen als `a` is gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="9cc73-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cc73-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="9cc73-113">Remarks</span></span>

<span data-ttu-id="9cc73-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="9cc73-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualB(a, b);
```