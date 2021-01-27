---
uid: Microsoft.Quantum.Logical.EqualB
title: De functie EqualB
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualB
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: 2a15a749f52fe814db4fa57118f69c80fa22158a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817258"
---
# <a name="equalb-function"></a><span data-ttu-id="f26e2-102">De functie EqualB</span><span class="sxs-lookup"><span data-stu-id="f26e2-102">EqualB function</span></span>

<span data-ttu-id="f26e2-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="f26e2-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="f26e2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f26e2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f26e2-105">Retourneert waar als en alleen als twee invoer waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="f26e2-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="f26e2-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f26e2-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="f26e2-107">a: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f26e2-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f26e2-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="f26e2-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="f26e2-109">b: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f26e2-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f26e2-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="f26e2-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f26e2-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f26e2-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="f26e2-112">`true` Als en alleen als `a` is gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="f26e2-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f26e2-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="f26e2-113">Remarks</span></span>

<span data-ttu-id="f26e2-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="f26e2-114">The following are equivalent:</span></span>

```qsharp
let cond = a == b;
let cond = EqualB(a, b);
```