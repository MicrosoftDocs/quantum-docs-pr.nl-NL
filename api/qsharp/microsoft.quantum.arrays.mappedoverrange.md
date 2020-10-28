---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: De functie MappedOverRange
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: e527a3ca1fd7571836f4f79bb453581f53d1db2b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705892"
---
# <a name="mappedoverrange-function"></a><span data-ttu-id="9ed34-102">De functie MappedOverRange</span><span class="sxs-lookup"><span data-stu-id="9ed34-102">MappedOverRange function</span></span>

<span data-ttu-id="9ed34-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9ed34-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9ed34-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9ed34-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9ed34-105">Op basis van een bereik en een functie die een geheel getal als invoer accepteert, retourneert een nieuwe matrix die bestaat uit de afbeeldingen van de bereik waarden onder de functie.</span><span class="sxs-lookup"><span data-stu-id="9ed34-105">Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.</span></span>

```qsharp
function MappedOverRange<'T> (mapper : (Int -> 'T), range : Range) : 'T[]
```


## <a name="input"></a><span data-ttu-id="9ed34-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9ed34-106">Input</span></span>

### <a name="mapper--int---t"></a><span data-ttu-id="9ed34-107">Mapper: [int](xref:microsoft.quantum.lang-ref.int) -> niet</span><span class="sxs-lookup"><span data-stu-id="9ed34-107">mapper : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="9ed34-108">Een functie van `Int` naar `'T` die wordt gebruikt om bereik waarden toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="9ed34-108">A function from `Int` to `'T` that is used to map range values.</span></span>


### <a name="range--range"></a><span data-ttu-id="9ed34-109">bereik: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="9ed34-109">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="9ed34-110">Een bereik van gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="9ed34-110">A range of integers.</span></span>



## <a name="output--t"></a><span data-ttu-id="9ed34-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="9ed34-111">Output : 'T[]</span></span>

<span data-ttu-id="9ed34-112">Een matrix `'T[]` van elementen die worden toegewezen door de `mapper` functie.</span><span class="sxs-lookup"><span data-stu-id="9ed34-112">An array `'T[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="9ed34-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9ed34-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9ed34-114">T</span><span class="sxs-lookup"><span data-stu-id="9ed34-114">'T</span></span>

<span data-ttu-id="9ed34-115">Het resultaat type van de `mapper` functie.</span><span class="sxs-lookup"><span data-stu-id="9ed34-115">The result type of the `mapper` function.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ed34-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="9ed34-116">Remarks</span></span>

<span data-ttu-id="9ed34-117">De functie is gedefinieerd voor algemene typen, d.w.z. Wanneer we een functie hebben, `mapper: Int -> 'T` kunnen we de waarden van het bereik toewijzen en een matrix van het type produceren `'T[]` .</span><span class="sxs-lookup"><span data-stu-id="9ed34-117">The function is defined for generic types, i.e., whenever we have a function `mapper: Int -> 'T` we can map the values of the range and produce an array of type `'T[]`.</span></span>

## <a name="see-also"></a><span data-ttu-id="9ed34-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9ed34-118">See Also</span></span>

- [<span data-ttu-id="9ed34-119">Micro soft. Quantum. arrays. toegewezen</span><span class="sxs-lookup"><span data-stu-id="9ed34-119">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)