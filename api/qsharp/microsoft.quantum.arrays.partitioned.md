---
uid: Microsoft.Quantum.Arrays.Partitioned
title: Gepartitioneerde functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Partitioned
qsharp.summary: Splits an array into multiple parts.
ms.openlocfilehash: e3395afeda206e255a58175b57245f91c588d978
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705845"
---
# <a name="partitioned-function"></a><span data-ttu-id="6d444-102">Gepartitioneerde functie</span><span class="sxs-lookup"><span data-stu-id="6d444-102">Partitioned function</span></span>

<span data-ttu-id="6d444-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6d444-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6d444-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6d444-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6d444-105">Hiermee splitst u een matrix in meerdere delen.</span><span class="sxs-lookup"><span data-stu-id="6d444-105">Splits an array into multiple parts.</span></span>

```qsharp
function Partitioned<'T> (nElements : Int[], arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="6d444-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="6d444-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="6d444-107">nElements: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="6d444-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="6d444-108">Aantal elementen in elk deel van de matrix</span><span class="sxs-lookup"><span data-stu-id="6d444-108">Number of elements in each part of array</span></span>


### <a name="arr--t"></a><span data-ttu-id="6d444-109">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="6d444-109">arr : 'T[]</span></span>

<span data-ttu-id="6d444-110">De invoer matrix die moet worden gesplitst.</span><span class="sxs-lookup"><span data-stu-id="6d444-110">Input array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="6d444-111">Uitvoer: ' [] []</span><span class="sxs-lookup"><span data-stu-id="6d444-111">Output : 'T[][]</span></span>

<span data-ttu-id="6d444-112">Meerdere matrices waarbij de eerste matrix het eerste is `nElements[0]` `arr` en de tweede matrix, `nElements[1]` `arr` enzovoort. De laatste matrix bevat alle resterende elementen.</span><span class="sxs-lookup"><span data-stu-id="6d444-112">Multiple arrays where the first array is the first `nElements[0]` of `arr` and the second array are the next `nElements[1]` of `arr` etc. The last array will contain all remaining elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6d444-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="6d444-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6d444-114">T</span><span class="sxs-lookup"><span data-stu-id="6d444-114">'T</span></span>

