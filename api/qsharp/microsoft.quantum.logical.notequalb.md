---
uid: Microsoft.Quantum.Logical.NotEqualB
title: De functie NotEqualB
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: NotEqualB
qsharp.summary: Returns true if and only if two inputs are not equal.
ms.openlocfilehash: 9f362b9e08f8a798bf7f7d9c323fee6576dccd9f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98814424"
---
# <a name="notequalb-function"></a><span data-ttu-id="cc104-102">De functie NotEqualB</span><span class="sxs-lookup"><span data-stu-id="cc104-102">NotEqualB function</span></span>

<span data-ttu-id="cc104-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="cc104-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="cc104-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cc104-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cc104-105">Retourneert waar als en alleen als twee invoer waarden niet gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="cc104-105">Returns true if and only if two inputs are not equal.</span></span>

```qsharp
function NotEqualB (a : Bool, b : Bool) : Bool
```


## <a name="input"></a><span data-ttu-id="cc104-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="cc104-106">Input</span></span>

### <a name="a--bool"></a><span data-ttu-id="cc104-107">a: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="cc104-107">a : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="cc104-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="cc104-108">The first value to be compared.</span></span>


### <a name="b--bool"></a><span data-ttu-id="cc104-109">b: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="cc104-109">b : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="cc104-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="cc104-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="cc104-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="cc104-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="cc104-112">`true` Als en alleen als `a` is niet gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="cc104-112">`true` if and only if `a` is not equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc104-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="cc104-113">Remarks</span></span>

<span data-ttu-id="cc104-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="cc104-114">The following are equivalent:</span></span>

```qsharp
let cond = a != b;
let cond = NotEqualB(a, b);
```