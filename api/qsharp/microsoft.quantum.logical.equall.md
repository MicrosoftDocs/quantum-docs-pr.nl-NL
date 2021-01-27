---
uid: Microsoft.Quantum.Logical.EqualL
title: De functie EQUAL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualL
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 58086f40ea20b6f1a5fa6996e3a6703e2bf66306
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98815970"
---
# <a name="equall-function"></a><span data-ttu-id="3664b-102">De functie EQUAL</span><span class="sxs-lookup"><span data-stu-id="3664b-102">EqualL function</span></span>

<span data-ttu-id="3664b-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="3664b-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="3664b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3664b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3664b-105">Retourneert waar als en alleen als twee invoer waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="3664b-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="3664b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="3664b-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="3664b-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="3664b-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="3664b-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="3664b-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="3664b-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="3664b-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="3664b-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="3664b-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="3664b-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3664b-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3664b-112">`true` Als en alleen als `a` is gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="3664b-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="3664b-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="3664b-113">Remarks</span></span>

<span data-ttu-id="3664b-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="3664b-114">The following are equivalent:</span></span>

```qsharp
let cond = a == b;
let cond = EqualL(a, b);
```