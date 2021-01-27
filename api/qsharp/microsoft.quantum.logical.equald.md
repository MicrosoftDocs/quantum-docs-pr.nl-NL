---
uid: Microsoft.Quantum.Logical.EqualD
title: Functie is gelijk aan
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: EqualD
qsharp.summary: Returns true if and only if two inputs are equal.
ms.openlocfilehash: f8a24d7bfb9b4f7b8b0e1f68a94bfb341716b024
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98816874"
---
# <a name="equald-function"></a><span data-ttu-id="c8e34-102">Functie is gelijk aan</span><span class="sxs-lookup"><span data-stu-id="c8e34-102">EqualD function</span></span>

<span data-ttu-id="c8e34-103">Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)</span><span class="sxs-lookup"><span data-stu-id="c8e34-103">Namespace: [Microsoft.Quantum.Logical](xref:Microsoft.Quantum.Logical)</span></span>

<span data-ttu-id="c8e34-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c8e34-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c8e34-105">Retourneert waar als en alleen als twee invoer waarden gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="c8e34-105">Returns true if and only if two inputs are equal.</span></span>

```qsharp
function EqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a><span data-ttu-id="c8e34-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c8e34-106">Input</span></span>

### <a name="a--double"></a><span data-ttu-id="c8e34-107">a: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c8e34-107">a : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c8e34-108">De eerste waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="c8e34-108">The first value to be compared.</span></span>


### <a name="b--double"></a><span data-ttu-id="c8e34-109">b: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="c8e34-109">b : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="c8e34-110">De tweede waarde die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="c8e34-110">The second value to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="c8e34-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="c8e34-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="c8e34-112">`true` Als en alleen als `a` is gelijk aan `b` .</span><span class="sxs-lookup"><span data-stu-id="c8e34-112">`true` if and only if `a` is equal to `b`.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8e34-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c8e34-113">Remarks</span></span>

<span data-ttu-id="c8e34-114">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="c8e34-114">The following are equivalent:</span></span>

```qsharp
let cond = a == b;
let cond = EqualD(a, b);
```