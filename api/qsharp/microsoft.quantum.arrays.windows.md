---
uid: Microsoft.Quantum.Arrays.Windows
title: Windows-functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: adfea2b9a2f6c22446817538d29586284dba723e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842199"
---
# <a name="windows-function"></a><span data-ttu-id="3f027-102">Windows-functie</span><span class="sxs-lookup"><span data-stu-id="3f027-102">Windows function</span></span>

<span data-ttu-id="3f027-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3f027-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3f027-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3f027-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3f027-105">Retourneert alle opeenvolgende submatrixen met een lengte `size` .</span><span class="sxs-lookup"><span data-stu-id="3f027-105">Returns all consecutive subarrays of length `size`.</span></span>

```qsharp
function Windows<'T> (size : Int, array : 'T[]) : 'T[][]
```


## <a name="description"></a><span data-ttu-id="3f027-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="3f027-106">Description</span></span>

<span data-ttu-id="3f027-107">Deze functie retourneert alle `n - size + 1` submatrixen met `size` een lengte in volg orde, waarbij `n` de lengte van is `arr` .</span><span class="sxs-lookup"><span data-stu-id="3f027-107">This function returns all `n - size + 1` subarrays of length `size` in order, where `n` is the length of `arr`.</span></span>
<span data-ttu-id="3f027-108">De eerste submatrixen bevinden zich `arr[0..size - 1], arr[1..size], arr[2..size + 1]` tot de laatste submatrix `arr[n - size..n - 1]` .</span><span class="sxs-lookup"><span data-stu-id="3f027-108">The first subarrays are `arr[0..size - 1], arr[1..size], arr[2..size + 1]` until the last subarray `arr[n - size..n - 1]`.</span></span>

<span data-ttu-id="3f027-109">Als `size <= 0` of `size > n` , wordt een lege matrix geretourneerd.</span><span class="sxs-lookup"><span data-stu-id="3f027-109">If `size <= 0` or `size > n`, an empty array is returned.</span></span>

## <a name="input"></a><span data-ttu-id="3f027-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="3f027-110">Input</span></span>

### <a name="size--int"></a><span data-ttu-id="3f027-111">grootte: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3f027-111">size : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3f027-112">De lengte van de submatrixen.</span><span class="sxs-lookup"><span data-stu-id="3f027-112">Length of the subarrays.</span></span>


### <a name="array--t"></a><span data-ttu-id="3f027-113">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="3f027-113">array : 'T[]</span></span>

<span data-ttu-id="3f027-114">Een matrix met elementen.</span><span class="sxs-lookup"><span data-stu-id="3f027-114">An array of elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="3f027-115">Uitvoer: ' [] []</span><span class="sxs-lookup"><span data-stu-id="3f027-115">Output : 'T[][]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3f027-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="3f027-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3f027-117">T</span><span class="sxs-lookup"><span data-stu-id="3f027-117">'T</span></span>

<span data-ttu-id="3f027-118">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="3f027-118">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="3f027-119">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="3f027-119">Example</span></span>

```qsharp
// same as [[1, 2, 3], [2, 3, 4], [3, 4, 5]]
let windows = Windows(3, [1, 2, 3, 4, 5]);
```