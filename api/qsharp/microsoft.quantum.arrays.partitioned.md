---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Gepartitioneerde functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: bce46262e3ef64a43e578098d81c5dd39225915e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220498"
---
# <a name="partitioned-function"></a><span data-ttu-id="55d1f-102">Gepartitioneerde functie</span><span class="sxs-lookup"><span data-stu-id="55d1f-102">Partitioned function</span></span>

<span data-ttu-id="55d1f-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="55d1f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="55d1f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="55d1f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="55d1f-105">Hiermee splitst u een matrix in meerdere delen.</span><span class="sxs-lookup"><span data-stu-id="55d1f-105">Splits an array into multiple parts.</span></span>

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="55d1f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="55d1f-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="55d1f-107">nElements: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="55d1f-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="55d1f-108">Aantal elementen in elk deel van de matrix</span><span class="sxs-lookup"><span data-stu-id="55d1f-108">Number of elements in each part of array</span></span>


### <a name="arr--t"></a><span data-ttu-id="55d1f-109">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="55d1f-109">arr : 'T[]</span></span>

<span data-ttu-id="55d1f-110">De invoer matrix die moet worden gesplitst.</span><span class="sxs-lookup"><span data-stu-id="55d1f-110">Input array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="55d1f-111">Uitvoer: ' [] []</span><span class="sxs-lookup"><span data-stu-id="55d1f-111">Output : 'T[][]</span></span>

<span data-ttu-id="55d1f-112">Meerdere matrices waarbij de eerste matrix het eerste is `nElements[0]` `arr` en de tweede matrix, `nElements[1]` `arr` enzovoort. De laatste matrix bevat alle resterende elementen.</span><span class="sxs-lookup"><span data-stu-id="55d1f-112">Multiple arrays where the first array is the first `nElements[0]` of `arr` and the second array are the next `nElements[1]` of `arr` etc. The last array will contain all remaining elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="55d1f-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="55d1f-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="55d1f-114">T</span><span class="sxs-lookup"><span data-stu-id="55d1f-114">'T</span></span>

