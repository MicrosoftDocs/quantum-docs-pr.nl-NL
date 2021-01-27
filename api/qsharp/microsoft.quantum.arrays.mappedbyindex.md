---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: De functie MappedByIndex
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 584cabcb7b6059ae5d311f13f5f75bd1f87bdba5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845669"
---
# <a name="mappedbyindex-function"></a><span data-ttu-id="6f65e-102">De functie MappedByIndex</span><span class="sxs-lookup"><span data-stu-id="6f65e-102">MappedByIndex function</span></span>

<span data-ttu-id="6f65e-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6f65e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6f65e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6f65e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6f65e-105">Op basis van een matrix en een functie die is gedefinieerd voor de geïndexeerde elementen van de matrix, retourneert een nieuwe matrix die bestaat uit de installatie kopieën van de oorspronkelijke matrix onder de functie.</span><span class="sxs-lookup"><span data-stu-id="6f65e-105">Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.</span></span>

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="6f65e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="6f65e-106">Input</span></span>

### <a name="mapper--intt---u"></a><span data-ttu-id="6f65e-107">Mapper: ([int](xref:microsoft.quantum.lang-ref.int), 't)-> ' U</span><span class="sxs-lookup"><span data-stu-id="6f65e-107">mapper : ([Int](xref:microsoft.quantum.lang-ref.int),'T) -> 'U</span></span>

<span data-ttu-id="6f65e-108">Een functie van `(Int, 'T)` naar `'U` die wordt gebruikt om elementen en hun indices toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="6f65e-108">A function from `(Int, 'T)` to `'U` that is used to map elements and their indices.</span></span>


### <a name="array--t"></a><span data-ttu-id="6f65e-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="6f65e-109">array : 'T[]</span></span>

<span data-ttu-id="6f65e-110">Een matrix van elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="6f65e-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="6f65e-111">Uitvoer: ' U []</span><span class="sxs-lookup"><span data-stu-id="6f65e-111">Output : 'U[]</span></span>

<span data-ttu-id="6f65e-112">Een matrix `'U[]` van elementen die worden toegewezen door de `mapper` functie.</span><span class="sxs-lookup"><span data-stu-id="6f65e-112">An array `'U[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6f65e-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="6f65e-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6f65e-114">T</span><span class="sxs-lookup"><span data-stu-id="6f65e-114">'T</span></span>

<span data-ttu-id="6f65e-115">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="6f65e-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="6f65e-116">' U</span><span class="sxs-lookup"><span data-stu-id="6f65e-116">'U</span></span>

<span data-ttu-id="6f65e-117">Het resultaat type van de `mapper` functie.</span><span class="sxs-lookup"><span data-stu-id="6f65e-117">The result type of the `mapper` function.</span></span>

## <a name="example"></a><span data-ttu-id="6f65e-118">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="6f65e-118">Example</span></span>

<span data-ttu-id="6f65e-119">De volgende twee regels zijn gelijk:</span><span class="sxs-lookup"><span data-stu-id="6f65e-119">The following two lines are equivalent:</span></span>

```qsharp
let arr = MapIndex(f, [x0, x1, x2]);
```

<span data-ttu-id="6f65e-120">en</span><span class="sxs-lookup"><span data-stu-id="6f65e-120">and</span></span>

```qsharp
let arr = [f(0, x0), f(1, x1), f(2, x2)];
```

## <a name="see-also"></a><span data-ttu-id="6f65e-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6f65e-121">See Also</span></span>

- [<span data-ttu-id="6f65e-122">Micro soft. Quantum. arrays. toegewezen</span><span class="sxs-lookup"><span data-stu-id="6f65e-122">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)