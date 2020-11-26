---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: De functie MappedOverRange
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: b1d73c2503e63ed09a3d6a56421760ca29eb0c3f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220685"
---
# <a name="mappedoverrange-function"></a><span data-ttu-id="8faf5-102">De functie MappedOverRange</span><span class="sxs-lookup"><span data-stu-id="8faf5-102">MappedOverRange function</span></span>

<span data-ttu-id="8faf5-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="8faf5-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="8faf5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8faf5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8faf5-105">Op basis van een bereik en een functie die een geheel getal als invoer accepteert, retourneert een nieuwe matrix die bestaat uit de afbeeldingen van de bereik waarden onder de functie.</span><span class="sxs-lookup"><span data-stu-id="8faf5-105">Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.</span></span>

```qsharp
function MappedOverRange<'T> (mapper : (Int -> 'T), range : Range) : 'T[]
```


## <a name="input"></a><span data-ttu-id="8faf5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="8faf5-106">Input</span></span>

### <a name="mapper--int---t"></a><span data-ttu-id="8faf5-107">Mapper: [int](xref:microsoft.quantum.lang-ref.int) -> niet</span><span class="sxs-lookup"><span data-stu-id="8faf5-107">mapper : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="8faf5-108">Een functie van `Int` naar `'T` die wordt gebruikt om bereik waarden toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="8faf5-108">A function from `Int` to `'T` that is used to map range values.</span></span>


### <a name="range--range"></a><span data-ttu-id="8faf5-109">bereik: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="8faf5-109">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="8faf5-110">Een bereik van gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="8faf5-110">A range of integers.</span></span>



## <a name="output--t"></a><span data-ttu-id="8faf5-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="8faf5-111">Output : 'T[]</span></span>

<span data-ttu-id="8faf5-112">Een matrix `'T[]` van elementen die worden toegewezen door de `mapper` functie.</span><span class="sxs-lookup"><span data-stu-id="8faf5-112">An array `'T[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="8faf5-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="8faf5-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8faf5-114">T</span><span class="sxs-lookup"><span data-stu-id="8faf5-114">'T</span></span>

<span data-ttu-id="8faf5-115">Het resultaat type van de `mapper` functie.</span><span class="sxs-lookup"><span data-stu-id="8faf5-115">The result type of the `mapper` function.</span></span>

## <a name="remarks"></a><span data-ttu-id="8faf5-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="8faf5-116">Remarks</span></span>

<span data-ttu-id="8faf5-117">De functie is gedefinieerd voor algemene typen, d.w.z. Wanneer we een functie hebben, `mapper: Int -> 'T` kunnen we de waarden van het bereik toewijzen en een matrix van het type produceren `'T[]` .</span><span class="sxs-lookup"><span data-stu-id="8faf5-117">The function is defined for generic types, i.e., whenever we have a function `mapper: Int -> 'T` we can map the values of the range and produce an array of type `'T[]`.</span></span>

## <a name="see-also"></a><span data-ttu-id="8faf5-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8faf5-118">See Also</span></span>

- [<span data-ttu-id="8faf5-119">Micro soft. Quantum. arrays. toegewezen</span><span class="sxs-lookup"><span data-stu-id="8faf5-119">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)