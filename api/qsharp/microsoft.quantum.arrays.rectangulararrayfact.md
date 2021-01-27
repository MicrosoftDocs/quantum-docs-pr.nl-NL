---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: De functie RectangularArrayFact
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: 8cf6b85da6e8fee7fc255a173753a6468d8134b9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845490"
---
# <a name="rectangulararrayfact-function"></a><span data-ttu-id="14333-102">De functie RectangularArrayFact</span><span class="sxs-lookup"><span data-stu-id="14333-102">RectangularArrayFact function</span></span>

<span data-ttu-id="14333-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="14333-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="14333-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="14333-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="14333-105">Vertegenwoordigt een voor waarde die een 2-dimensionale matrix heeft met een rechthoekige vorm</span><span class="sxs-lookup"><span data-stu-id="14333-105">Represents a condition that a 2-dimensional array has a rectangular shape</span></span>

```qsharp
function RectangularArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="14333-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="14333-106">Description</span></span>

<span data-ttu-id="14333-107">Deze functie beweringt dat elke rij in een matrix dezelfde lengte heeft.</span><span class="sxs-lookup"><span data-stu-id="14333-107">This function asserts that each row in an array has the same length.</span></span>

## <a name="input"></a><span data-ttu-id="14333-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="14333-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="14333-109">matrix: ' [] []</span><span class="sxs-lookup"><span data-stu-id="14333-109">array : 'T[][]</span></span>

<span data-ttu-id="14333-110">Een 2-dimensionale matrix van elementen</span><span class="sxs-lookup"><span data-stu-id="14333-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="14333-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="14333-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="14333-112">Een bericht dat moet worden afgedrukt als de matrix geen rechthoekige matrix is</span><span class="sxs-lookup"><span data-stu-id="14333-112">A message to be printed if the array is not a rectangular array</span></span>



## <a name="output--unit"></a><span data-ttu-id="14333-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="14333-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="14333-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="14333-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="14333-115">T</span><span class="sxs-lookup"><span data-stu-id="14333-115">'T</span></span>

<span data-ttu-id="14333-116">Het type van elk element van `array` .</span><span class="sxs-lookup"><span data-stu-id="14333-116">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="14333-117">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="14333-117">Example</span></span>

```qsharp
RectangularArrayFact([[1, 2], [3, 4]], "Array is not rectangular");       // okay
RectangularArrayFact([[1, 2, 3], [4, 5, 6]], "Array is not rectangular"); // okay
RectangularArrayFact([[1, 2], [3, 4, 5]], "Array is not rectangular");    // will fail
```

## <a name="see-also"></a><span data-ttu-id="14333-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="14333-118">See Also</span></span>

- [<span data-ttu-id="14333-119">Micro soft. Quantum. arrays. SquareArrayFact</span><span class="sxs-lookup"><span data-stu-id="14333-119">Microsoft.Quantum.Arrays.SquareArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.SquareArrayFact)