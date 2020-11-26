---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: De functie MappedByIndex
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 430495517974b641c249fa146aa9effec542e825
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209924"
---
# <a name="mappedbyindex-function"></a><span data-ttu-id="5bcf9-102">De functie MappedByIndex</span><span class="sxs-lookup"><span data-stu-id="5bcf9-102">MappedByIndex function</span></span>

<span data-ttu-id="5bcf9-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="5bcf9-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="5bcf9-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5bcf9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5bcf9-105">Op basis van een matrix en een functie die is gedefinieerd voor de geïndexeerde elementen van de matrix, retourneert een nieuwe matrix die bestaat uit de installatie kopieën van de oorspronkelijke matrix onder de functie.</span><span class="sxs-lookup"><span data-stu-id="5bcf9-105">Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="5bcf9-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5bcf9-106">Input</span></span>

### <a name="mapper--intt---u"></a><span data-ttu-id="5bcf9-107">Mapper: ([int](xref:microsoft.quantum.lang-ref.int), 't)-> ' U</span><span class="sxs-lookup"><span data-stu-id="5bcf9-107">mapper : ([Int](xref:microsoft.quantum.lang-ref.int),'T) -> 'U</span></span>

<span data-ttu-id="5bcf9-108">Een functie van `(Int, 'T)` naar `'U` die wordt gebruikt om elementen en hun indices toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="5bcf9-108">A function from `(Int, 'T)` to `'U` that is used to map elements and their indices.</span></span>


### <a name="array--t"></a><span data-ttu-id="5bcf9-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="5bcf9-109">array : 'T[]</span></span>

<span data-ttu-id="5bcf9-110">Een matrix van elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="5bcf9-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="5bcf9-111">Uitvoer: ' U []</span><span class="sxs-lookup"><span data-stu-id="5bcf9-111">Output : 'U[]</span></span>

<span data-ttu-id="5bcf9-112">Een matrix `'U[]` van elementen die worden toegewezen door de `mapper` functie.</span><span class="sxs-lookup"><span data-stu-id="5bcf9-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5bcf9-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="5bcf9-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5bcf9-114">T</span><span class="sxs-lookup"><span data-stu-id="5bcf9-114">'T</span></span>

<span data-ttu-id="5bcf9-115">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="5bcf9-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="5bcf9-116">' U</span><span class="sxs-lookup"><span data-stu-id="5bcf9-116">'U</span></span>

<span data-ttu-id="5bcf9-117">Het resultaat type van de `mapper` functie.</span><span class="sxs-lookup"><span data-stu-id="5bcf9-117">The result type of the `mapper` function.</span></span>

## <a name="see-also"></a><span data-ttu-id="5bcf9-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5bcf9-118">See Also</span></span>

- [<span data-ttu-id="5bcf9-119">Micro soft. Quantum. arrays. toegewezen</span><span class="sxs-lookup"><span data-stu-id="5bcf9-119">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)