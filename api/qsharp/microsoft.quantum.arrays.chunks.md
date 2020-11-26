---
uid: Microsoft.Quantum.Arrays.Chunks
title: De functie chunks
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: b323fdab1b207c72a4f46d5ca4cb368ecf0df818
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221603"
---
# <a name="chunks-function"></a><span data-ttu-id="0977d-102">De functie chunks</span><span class="sxs-lookup"><span data-stu-id="0977d-102">Chunks function</span></span>

<span data-ttu-id="0977d-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="0977d-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="0977d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0977d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0977d-105">Splitst een matrix in meerdere delen van gelijke lengte.</span><span class="sxs-lookup"><span data-stu-id="0977d-105">Splits an array into multiple parts of equal length.</span></span>

```qsharp
function Chunks<'T> (nElements : Int, arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="0977d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="0977d-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="0977d-107">nElements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="0977d-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="0977d-108">De lengte van elk segment.</span><span class="sxs-lookup"><span data-stu-id="0977d-108">The length of each chunk.</span></span>


### <a name="arr--t"></a><span data-ttu-id="0977d-109">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="0977d-109">arr : 'T[]</span></span>

<span data-ttu-id="0977d-110">De matrix die moet worden gesplitst.</span><span class="sxs-lookup"><span data-stu-id="0977d-110">The array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="0977d-111">Uitvoer: ' [] []</span><span class="sxs-lookup"><span data-stu-id="0977d-111">Output : 'T[][]</span></span>

<span data-ttu-id="0977d-112">Een matrix met elk segment van de oorspronkelijke matrix.</span><span class="sxs-lookup"><span data-stu-id="0977d-112">A array containing each chunk of the original array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="0977d-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="0977d-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0977d-114">T</span><span class="sxs-lookup"><span data-stu-id="0977d-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="0977d-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="0977d-115">Remarks</span></span>

<span data-ttu-id="0977d-116">Houd er rekening mee dat het laatste element van de uitvoer mogelijk korter `nElements` is dan of `Length(arr)` niet deelbaar is door `nElements` .</span><span class="sxs-lookup"><span data-stu-id="0977d-116">Note that the last element of the output may be shorter than `nElements` if `Length(arr)` is not divisible by `nElements`.</span></span>