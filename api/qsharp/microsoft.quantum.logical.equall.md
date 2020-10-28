---
uid: Microsoft.Quantum.Logical.EqualL
title: De functie EQUAL
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualL
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: f0a2bfa866068746e9c6e249573eb61c0d08c0f0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701498"
---
# <a name="equall-function"></a><span data-ttu-id="2b954-102">De functie EQUAL</span><span class="sxs-lookup"><span data-stu-id="2b954-102">EqualL function</span></span>

<span data-ttu-id="2b954-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="2b954-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="2b954-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2b954-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2b954-105">Retourneert waar als en alleen als twee invoer waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="2b954-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="2b954-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="2b954-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="2b954-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2b954-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2b954-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="2b954-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="2b954-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="2b954-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="2b954-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="2b954-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="2b954-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2b954-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="2b954-112">`true` Als en alleen als `a` is gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="2b954-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b954-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="2b954-113">Remarks</span></span>

<span data-ttu-id="2b954-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="2b954-114">The following are equivalent:</span></span>

```Q#
let cond = a == b;
let cond = EqualL(a, b);
```