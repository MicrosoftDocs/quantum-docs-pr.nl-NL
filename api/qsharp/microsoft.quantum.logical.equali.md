---
uid: Microsoft.Quantum.Logical.EqualI
title: De functie EqualI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualI
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 87cf00ea8bb738cda30092b3d80940291beb1fb9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98816755"
---
# <a name="equali-function"></a><span data-ttu-id="d8569-102">De functie EqualI</span><span class="sxs-lookup"><span data-stu-id="d8569-102">EqualI function</span></span>

<span data-ttu-id="d8569-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="d8569-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="d8569-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d8569-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d8569-105">Retourneert waar als en alleen als twee invoer waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="d8569-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a><span data-ttu-id="d8569-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d8569-106">Input</span></span>

### <a name="a--int"></a><span data-ttu-id="d8569-107">a: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d8569-107">a : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d8569-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="d8569-108">The first value to be compared.</span></span>


### <a name="b--int"></a><span data-ttu-id="d8569-109">b: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d8569-109">b : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d8569-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="d8569-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="d8569-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d8569-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d8569-112">`true` Als en alleen als `a` is gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="d8569-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8569-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d8569-113">Remarks</span></span>

<span data-ttu-id="d8569-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="d8569-114">The following are equivalent:</span></span>

```qsharp
let cond = a == b;
let cond = EqualI(a, b);
```