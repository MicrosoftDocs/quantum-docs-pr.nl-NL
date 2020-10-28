---
uid: Microsoft.Quantum.Logical.NotEqualL
title: De functie NotEqualL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualL
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: f1d36c284293519e75e6c30ac64679c7bdf4609c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701397"
---
# <a name="notequall-function"></a><span data-ttu-id="9ff04-102">De functie NotEqualL</span><span class="sxs-lookup"><span data-stu-id="9ff04-102">NotEqualL function</span></span>

<span data-ttu-id="9ff04-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="9ff04-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="9ff04-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9ff04-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9ff04-105">Retourneert waar als en alleen als twee invoer waarden niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="9ff04-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="9ff04-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9ff04-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="9ff04-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9ff04-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9ff04-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="9ff04-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="9ff04-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="9ff04-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="9ff04-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="9ff04-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="9ff04-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9ff04-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9ff04-112">`true` Als en alleen als `a` is niet gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="9ff04-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ff04-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="9ff04-113">Remarks</span></span>

<span data-ttu-id="9ff04-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="9ff04-114">The following are equivalent:</span></span>

```Q#
let cond = a != b;
let cond = NotEqualL(a, b);
```