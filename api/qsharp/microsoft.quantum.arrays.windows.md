---
uid: Microsoft.Quantum.Arrays.Windows
title: Windows-functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: 6071d1c3e5981855c57abd0e741b1de0201c30a3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705693"
---
# <a name="windows-function"></a><span data-ttu-id="54eb8-102">Windows-functie</span><span class="sxs-lookup"><span data-stu-id="54eb8-102">Windows function</span></span>

<span data-ttu-id="54eb8-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="54eb8-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="54eb8-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="54eb8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="54eb8-105">Retourneert alle opeenvolgende submatrixen met een lengte `size` .</span><span class="sxs-lookup"><span data-stu-id="54eb8-105">Returns all consecutive subarrays of length `size`.</span></span>

```qsharp
function Windows<'T> (size : Int, array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="54eb8-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="54eb8-106">Description</span></span>

<span data-ttu-id="54eb8-107">Deze functie retourneert alle `n - size + 1` submatrixen met `size` een lengte in volg orde, waarbij `n` de lengte van is `arr` .</span><span class="sxs-lookup"><span data-stu-id="54eb8-107">This function returns all `n - size + 1` subarrays of length `size` in order, where `n` is the length of `arr`.</span></span>
<span data-ttu-id="54eb8-108">De eerste submatrixen bevinden zich `arr[0..size - 1], arr[1..size], arr[2..size + 1]` tot de laatste submatrix `arr[n - size..n - 1]` .</span><span class="sxs-lookup"><span data-stu-id="54eb8-108">The first subarrays are `arr[0..size - 1], arr[1..size], arr[2..size + 1]` until the last subarray `arr[n - size..n - 1]`.</span></span>

<span data-ttu-id="54eb8-109">Als `size <= 0` of `size > n` , wordt een lege matrix geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="54eb8-109">If `size <= 0` or `size > n`, an empty array is returned.</span></span>

## <a name="input"></a><span data-ttu-id="54eb8-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="54eb8-110">Input</span></span>

### <a name="size--int"></a><span data-ttu-id="54eb8-111">grootte: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="54eb8-111">size : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="54eb8-112">De lengte van de submatrixen.</span><span class="sxs-lookup"><span data-stu-id="54eb8-112">Length of the subarrays.</span></span>


### <a name="array--t"></a><span data-ttu-id="54eb8-113">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="54eb8-113">array : 'T[]</span></span>

<span data-ttu-id="54eb8-114">Een matrix met elementen.</span><span class="sxs-lookup"><span data-stu-id="54eb8-114">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="54eb8-115">Uitvoer: ' [] []</span><span class="sxs-lookup"><span data-stu-id="54eb8-115">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="54eb8-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="54eb8-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="54eb8-117">T</span><span class="sxs-lookup"><span data-stu-id="54eb8-117">'T</span></span>

<span data-ttu-id="54eb8-118">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="54eb8-118">The type of `array` elements.</span></span>