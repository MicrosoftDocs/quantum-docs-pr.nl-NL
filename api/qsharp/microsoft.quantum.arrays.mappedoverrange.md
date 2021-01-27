---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: De functie MappedOverRange
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: 7093043e2a290e6132774b8fe154d3627a254f27
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845639"
---
# <a name="mappedoverrange-function"></a><span data-ttu-id="3a41f-102">De functie MappedOverRange</span><span class="sxs-lookup"><span data-stu-id="3a41f-102">MappedOverRange function</span></span>

<span data-ttu-id="3a41f-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3a41f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3a41f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3a41f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3a41f-105">Op basis van een bereik en een functie die een geheel getal als invoer accepteert, retourneert een nieuwe matrix die bestaat uit de afbeeldingen van de bereik waarden onder de functie.</span><span class="sxs-lookup"><span data-stu-id="3a41f-105">Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.</span></span>

```qsharp
function MappedOverRange<'T> (mapper : (Int -> 'T), range : Range) : 'T[]
```


## <a name="input"></a><span data-ttu-id="3a41f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="3a41f-106">Input</span></span>

### <a name="mapper--int---t"></a><span data-ttu-id="3a41f-107">Mapper: [int](xref:microsoft.quantum.lang-ref.int) -> niet</span><span class="sxs-lookup"><span data-stu-id="3a41f-107">mapper : [Int](xref:microsoft.quantum.lang-ref.int) -> 'T</span></span>

<span data-ttu-id="3a41f-108">Een functie van `Int` naar `'T` die wordt gebruikt om bereik waarden toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="3a41f-108">A function from `Int` to `'T` that is used to map range values.</span></span>


### <a name="range--range"></a><span data-ttu-id="3a41f-109">bereik: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="3a41f-109">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="3a41f-110">Een bereik van gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="3a41f-110">A range of integers.</span></span>



## <a name="output--t"></a><span data-ttu-id="3a41f-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="3a41f-111">Output : 'T[]</span></span>

<span data-ttu-id="3a41f-112">Een matrix `'T[]` van elementen die worden toegewezen door de `mapper` functie.</span><span class="sxs-lookup"><span data-stu-id="3a41f-112">An array `'T[]` of elements that are mapped by the `mapper` function.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3a41f-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="3a41f-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3a41f-114">T</span><span class="sxs-lookup"><span data-stu-id="3a41f-114">'T</span></span>

<span data-ttu-id="3a41f-115">Het resultaat type van de `mapper` functie.</span><span class="sxs-lookup"><span data-stu-id="3a41f-115">The result type of the `mapper` function.</span></span>

## <a name="example"></a><span data-ttu-id="3a41f-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="3a41f-116">Example</span></span>

<span data-ttu-id="3a41f-117">In dit voor beeld wordt 1 toegevoegd aan een bereik van even cijfers:</span><span class="sxs-lookup"><span data-stu-id="3a41f-117">This example adds 1 to a range of even numbers:</span></span>

```qsharp
let numbers = MappedOverRange(PlusI(1, _), 0..2..10);
// numbers = [1, 3, 5, 7, 9, 11]
```

## <a name="remarks"></a><span data-ttu-id="3a41f-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="3a41f-118">Remarks</span></span>

<span data-ttu-id="3a41f-119">De functie is gedefinieerd voor algemene typen, d.w.z. Wanneer we een functie hebben, `mapper: Int -> 'T` kunnen we de waarden van het bereik toewijzen en een matrix van het type produceren `'T[]` .</span><span class="sxs-lookup"><span data-stu-id="3a41f-119">The function is defined for generic types, i.e., whenever we have a function `mapper: Int -> 'T` we can map the values of the range and produce an array of type `'T[]`.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a41f-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3a41f-120">See Also</span></span>

- [<span data-ttu-id="3a41f-121">Micro soft. Quantum. arrays. toegewezen</span><span class="sxs-lookup"><span data-stu-id="3a41f-121">Microsoft.Quantum.Arrays.Mapped</span></span>](xref:Microsoft.Quantum.Arrays.Mapped)