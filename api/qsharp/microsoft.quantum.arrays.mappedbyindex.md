---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: De functie MappedByIndex
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 07ca523248c363f2229551a14e77803dc4f4f82e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705900"
---
# <a name="mappedbyindex-function"></a><span data-ttu-id="bb43c-102">De functie MappedByIndex</span><span class="sxs-lookup"><span data-stu-id="bb43c-102">MappedByIndex function</span></span>

<span data-ttu-id="bb43c-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="bb43c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="bb43c-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bb43c-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bb43c-105">Op basis van een matrix en een functie die is gedefinieerd voor de geïndexeerde elementen van de matrix, retourneert een nieuwe matrix die bestaat uit de installatie kopieën van de oorspronkelijke matrix onder de functie.</span><span class="sxs-lookup"><span data-stu-id="bb43c-105">Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="bb43c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="bb43c-106">Input</span></span>

### <a name="mapper--intt---u"></a><span data-ttu-id="bb43c-107">Mapper: ([int](xref:microsoft.quantum.lang-ref.int), 't)-> ' U</span><span class="sxs-lookup"><span data-stu-id="bb43c-107">mapper : ([Int](xref:microsoft.quantum.lang-ref.int),'T) -> 'U</span></span>

<span data-ttu-id="bb43c-108">Een functie van `(Int, 'T)` naar `'U` die wordt gebruikt om elementen en hun indices toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="bb43c-108">A function from `(Int, 'T)` to `'U` that is used to map elements and their indices.</span></span>


### <a name="array--t"></a><span data-ttu-id="bb43c-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="bb43c-109">array : 'T[]</span></span>

<span data-ttu-id="bb43c-110">Een matrix van elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="bb43c-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="bb43c-111">Uitvoer: ' U []</span><span class="sxs-lookup"><span data-stu-id="bb43c-111">Output : 'U[]</span></span>

<span data-ttu-id="bb43c-112">Een matrix `'U[]` van elementen die worden toegewezen door de `mapper` functie.</span><span class="sxs-lookup"><span data-stu-id="bb43c-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="bb43c-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="bb43c-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="bb43c-114">T</span><span class="sxs-lookup"><span data-stu-id="bb43c-114">'T</span></span>

<span data-ttu-id="bb43c-115">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="bb43c-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="bb43c-116">' U</span><span class="sxs-lookup"><span data-stu-id="bb43c-116">'U</span></span>

<span data-ttu-id="bb43c-117">Het resultaat type van de `mapper` functie.</span><span class="sxs-lookup"><span data-stu-id="bb43c-117">The result type of the `mapper` function.</span></span>

## <a name="see-also"></a><span data-ttu-id="bb43c-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="bb43c-118">See Also</span></span>

- [<span data-ttu-id="bb43c-119">Micro soft. Quantum. arrays. toegewezen</span><span class="sxs-lookup"><span data-stu-id="bb43c-119">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)