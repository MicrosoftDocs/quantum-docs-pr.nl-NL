---
uid: Microsoft.Quantum.Synthesis.DecomposedOn
title: De functie DecomposedOn
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: DecomposedOn
qsharp.summary: Decomposes a permutation on a variable
ms.openlocfilehash: b033723a50fb85e77c9d4baec1f94231327e9b25
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709174"
---
# <a name="decomposedon-function"></a><span data-ttu-id="528e3-102">De functie DecomposedOn</span><span class="sxs-lookup"><span data-stu-id="528e3-102">DecomposedOn function</span></span>

<span data-ttu-id="528e3-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="528e3-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="528e3-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="528e3-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="528e3-105">Ontleedt een permutatie op een variabele</span><span class="sxs-lookup"><span data-stu-id="528e3-105">Decomposes a permutation on a variable</span></span>

```qsharp
function DecomposedOn (perm : Int[], index : Int) : ((Int[], Int[]), Int[])
```


## <a name="description"></a><span data-ttu-id="528e3-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="528e3-106">Description</span></span>

<span data-ttu-id="528e3-107">Met een permutatie $ \pi $ ( `perm` ) en een index $i $ ( `index` ), deze methode retourneert drie permutaties $ ((\ pi_l, \ pi_r), \pi ') $ zo dat de installatie kopieën van $ \ pi_l $ en $ \ pi_r $ geen bits in hun eigen elementen wijzigen op andere indexen dan $i $ en installatie kopieën van $ \pi $ in hun eigen elementen.</span><span class="sxs-lookup"><span data-stu-id="528e3-107">Given a permutation $\pi$ (`perm`) and an index $i$ (`index`), this method returns three permutations $((\pi_l, \pi_r), \pi')$ such that the images of $\pi_l$ and $\pi_r$ do not change bits in their elements at indexes other than $i$ and images of $\pi'$ do not change bit $i$ in their elements.</span></span>

## <a name="input"></a><span data-ttu-id="528e3-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="528e3-108">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="528e3-109">macht: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="528e3-109">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>




### <a name="index--int"></a><span data-ttu-id="528e3-110">index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="528e3-110">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>





## <a name="output--intintint"></a><span data-ttu-id="528e3-111">Output: (([int](xref:microsoft.quantum.lang-ref.int)[],[int](xref:microsoft.quantum.lang-ref.int)[]),[int](xref:microsoft.quantum.lang-ref.int)[])</span><span class="sxs-lookup"><span data-stu-id="528e3-111">Output : (([Int](xref:microsoft.quantum.lang-ref.int)[],[Int](xref:microsoft.quantum.lang-ref.int)[]),[Int](xref:microsoft.quantum.lang-ref.int)[])</span></span>

