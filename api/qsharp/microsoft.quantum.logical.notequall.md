---
uid: Microsoft.Quantum.Logical.NotEqualL
title: De functie NotEqualL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualL
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: b19de2e4e8052c77118f341700357b212e20af53
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849026"
---
# <a name="notequall-function"></a><span data-ttu-id="ebbff-102">De functie NotEqualL</span><span class="sxs-lookup"><span data-stu-id="ebbff-102">NotEqualL function</span></span>

<span data-ttu-id="ebbff-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="ebbff-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="ebbff-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ebbff-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ebbff-105">Retourneert waar als en alleen als twee invoer waarden niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="ebbff-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a><span data-ttu-id="ebbff-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ebbff-106">Input</span></span>

### <a name="a--bigint"></a><span data-ttu-id="ebbff-107">a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="ebbff-107">a : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="ebbff-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="ebbff-108">The first value to be compared.</span></span>


### <a name="b--bigint"></a><span data-ttu-id="ebbff-109">b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="ebbff-109">b : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="ebbff-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="ebbff-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="ebbff-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="ebbff-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="ebbff-112">`true` Als en alleen als `a` is niet gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="ebbff-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebbff-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="ebbff-113">Remarks</span></span>

<span data-ttu-id="ebbff-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="ebbff-114">The following are equivalent:</span></span>

```qsharp
let cond = a != b;
let cond = NotEqualL(a, b);
```