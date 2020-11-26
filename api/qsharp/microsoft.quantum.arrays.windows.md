---
uid: Microsoft.Quantum.Arrays.Windows
title: Windows-functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: 8f32a23aa4379744b84c3b8d9c8f565e61c3c64e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219886"
---
# <a name="windows-function"></a><span data-ttu-id="f3a5b-102">Windows-functie</span><span class="sxs-lookup"><span data-stu-id="f3a5b-102">Windows function</span></span>

<span data-ttu-id="f3a5b-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f3a5b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f3a5b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f3a5b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f3a5b-105">Retourneert alle opeenvolgende submatrixen met een lengte `size` .</span><span class="sxs-lookup"><span data-stu-id="f3a5b-105">Returns all consecutive subarrays of length `size`.</span></span>

```qsharp
function Windows<'T> (size : Int, array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="f3a5b-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f3a5b-106">Description</span></span>

<span data-ttu-id="f3a5b-107">Deze functie retourneert alle `n - size + 1` submatrixen met `size` een lengte in volg orde, waarbij `n` de lengte van is `arr` .</span><span class="sxs-lookup"><span data-stu-id="f3a5b-107">This function returns all `n - size + 1` subarrays of length `size` in order, where `n` is the length of `arr`.</span></span>
<span data-ttu-id="f3a5b-108">De eerste submatrixen bevinden zich `arr[0..size - 1], arr[1..size], arr[2..size + 1]` tot de laatste submatrix `arr[n - size..n - 1]` .</span><span class="sxs-lookup"><span data-stu-id="f3a5b-108">The first subarrays are `arr[0..size - 1], arr[1..size], arr[2..size + 1]` until the last subarray `arr[n - size..n - 1]`.</span></span>

<span data-ttu-id="f3a5b-109">Als `size <= 0` of `size > n` , wordt een lege matrix geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="f3a5b-109">If `size <= 0` or `size > n`, an empty array is returned.</span></span>

## <a name="input"></a><span data-ttu-id="f3a5b-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="f3a5b-110">Input</span></span>

### <a name="size--int"></a><span data-ttu-id="f3a5b-111">grootte: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f3a5b-111">size : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f3a5b-112">De lengte van de submatrixen.</span><span class="sxs-lookup"><span data-stu-id="f3a5b-112">Length of the subarrays.</span></span>


### <a name="array--t"></a><span data-ttu-id="f3a5b-113">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="f3a5b-113">array : 'T[]</span></span>

<span data-ttu-id="f3a5b-114">Een matrix met elementen.</span><span class="sxs-lookup"><span data-stu-id="f3a5b-114">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="f3a5b-115">Uitvoer: ' [] []</span><span class="sxs-lookup"><span data-stu-id="f3a5b-115">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f3a5b-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="f3a5b-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f3a5b-117">T</span><span class="sxs-lookup"><span data-stu-id="f3a5b-117">'T</span></span>

<span data-ttu-id="f3a5b-118">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="f3a5b-118">The type of `array` elements.</span></span>