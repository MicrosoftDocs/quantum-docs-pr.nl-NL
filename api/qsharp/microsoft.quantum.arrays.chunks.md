---
uid: Microsoft.Quantum.Arrays.Chunks
title: De functie chunks
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: 977594839a7d2fe09de8138d32a4a50e8a752390
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842878"
---
# <a name="chunks-function"></a><span data-ttu-id="11eb2-102">De functie chunks</span><span class="sxs-lookup"><span data-stu-id="11eb2-102">Chunks function</span></span>

<span data-ttu-id="11eb2-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="11eb2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="11eb2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="11eb2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="11eb2-105">Splitst een matrix in meerdere delen van gelijke lengte.</span><span class="sxs-lookup"><span data-stu-id="11eb2-105">Splits an array into multiple parts of equal length.</span></span>

```qsharp
function Chunks<'T> (nElements : Int, arr : 'T[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="11eb2-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="11eb2-106">Input</span></span>

### <a name="nelements--int"></a><span data-ttu-id="11eb2-107">nElements: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="11eb2-107">nElements : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="11eb2-108">De lengte van elk segment.</span><span class="sxs-lookup"><span data-stu-id="11eb2-108">The length of each chunk.</span></span>


### <a name="arr--t"></a><span data-ttu-id="11eb2-109">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="11eb2-109">arr : 'T[]</span></span>

<span data-ttu-id="11eb2-110">De matrix die moet worden gesplitst.</span><span class="sxs-lookup"><span data-stu-id="11eb2-110">The array to be split.</span></span>



## <a name="output--t"></a><span data-ttu-id="11eb2-111">Uitvoer: ' [] []</span><span class="sxs-lookup"><span data-stu-id="11eb2-111">Output : 'T[][]</span></span>

<span data-ttu-id="11eb2-112">Een matrix met elk segment van de oorspronkelijke matrix.</span><span class="sxs-lookup"><span data-stu-id="11eb2-112">A array containing each chunk of the original array.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="11eb2-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="11eb2-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="11eb2-114">T</span><span class="sxs-lookup"><span data-stu-id="11eb2-114">'T</span></span>



## <a name="remarks"></a><span data-ttu-id="11eb2-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="11eb2-115">Remarks</span></span>

<span data-ttu-id="11eb2-116">Houd er rekening mee dat het laatste element van de uitvoer mogelijk korter `nElements` is dan of `Length(arr)` niet deelbaar is door `nElements` .</span><span class="sxs-lookup"><span data-stu-id="11eb2-116">Note that the last element of the output may be shorter than `nElements` if `Length(arr)` is not divisible by `nElements`.</span></span>