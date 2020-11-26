---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: De functie RectangularArrayFact
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: b8ef7d52f7f815ca3e21ded1236e775a381646cb
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220413"
---
# <a name="rectangulararrayfact-function"></a><span data-ttu-id="e15f2-102">De functie RectangularArrayFact</span><span class="sxs-lookup"><span data-stu-id="e15f2-102">RectangularArrayFact function</span></span>

<span data-ttu-id="e15f2-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e15f2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e15f2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e15f2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e15f2-105">Vertegenwoordigt een voor waarde die een 2-dimensionale matrix heeft met een rechthoekige vorm</span><span class="sxs-lookup"><span data-stu-id="e15f2-105">Represents a condition that a 2-dimensional array has a rectangular shape</span></span>

```qsharp
function RectangularArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="e15f2-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e15f2-106">Description</span></span>

<span data-ttu-id="e15f2-107">Deze functie beweringt dat elke rij in een matrix dezelfde lengte heeft.</span><span class="sxs-lookup"><span data-stu-id="e15f2-107">This function asserts that each row in an array has the same length.</span></span>

## <a name="input"></a><span data-ttu-id="e15f2-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="e15f2-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="e15f2-109">matrix: ' [] []</span><span class="sxs-lookup"><span data-stu-id="e15f2-109">array : 'T[][]</span></span>

<span data-ttu-id="e15f2-110">Een 2-dimensionale matrix van elementen</span><span class="sxs-lookup"><span data-stu-id="e15f2-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="e15f2-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="e15f2-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="e15f2-112">Een bericht dat moet worden afgedrukt als de matrix geen rechthoekige matrix is</span><span class="sxs-lookup"><span data-stu-id="e15f2-112">A message to be printed if the array is not a rectangular array</span></span>



## <a name="output--unit"></a><span data-ttu-id="e15f2-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e15f2-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e15f2-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e15f2-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e15f2-115">T</span><span class="sxs-lookup"><span data-stu-id="e15f2-115">'T</span></span>

<span data-ttu-id="e15f2-116">Het type van elk element van `array` .</span><span class="sxs-lookup"><span data-stu-id="e15f2-116">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="e15f2-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e15f2-117">See Also</span></span>

- [<span data-ttu-id="e15f2-118">Micro soft. Quantum. arrays. SquareArrayFact</span><span class="sxs-lookup"><span data-stu-id="e15f2-118">Microsoft.Quantum.Arrays.SquareArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.SquareArrayFact)