---
uid: Microsoft.Quantum.Arrays.RectangularArrayFact
title: De functie RectangularArrayFact
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: RectangularArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a rectangular shape
ms.openlocfilehash: f0d3f4d6bfa9e86f1c7a91792c09e16fe86433a0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705812"
---
# <a name="rectangulararrayfact-function"></a><span data-ttu-id="9d952-102">De functie RectangularArrayFact</span><span class="sxs-lookup"><span data-stu-id="9d952-102">RectangularArrayFact function</span></span>

<span data-ttu-id="9d952-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9d952-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9d952-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9d952-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9d952-105">Vertegenwoordigt een voor waarde die een 2-dimensionale matrix heeft met een rechthoekige vorm</span><span class="sxs-lookup"><span data-stu-id="9d952-105">Represents a condition that a 2-dimensional array has a rectangular shape</span></span>

```qsharp
function RectangularArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="9d952-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="9d952-106">Description</span></span>

<span data-ttu-id="9d952-107">Deze functie beweringt dat elke rij in een matrix dezelfde lengte heeft.</span><span class="sxs-lookup"><span data-stu-id="9d952-107">This function asserts that each row in an array has the same length.</span></span>

## <a name="input"></a><span data-ttu-id="9d952-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="9d952-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="9d952-109">matrix: ' [] []</span><span class="sxs-lookup"><span data-stu-id="9d952-109">array : 'T[][]</span></span>

<span data-ttu-id="9d952-110">Een 2-dimensionale matrix van elementen</span><span class="sxs-lookup"><span data-stu-id="9d952-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="9d952-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="9d952-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="9d952-112">Een bericht dat moet worden afgedrukt als de matrix geen rechthoekige matrix is</span><span class="sxs-lookup"><span data-stu-id="9d952-112">A message to be printed if the array is not a rectangular array</span></span>



## <a name="output--unit"></a><span data-ttu-id="9d952-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9d952-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9d952-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9d952-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9d952-115">T</span><span class="sxs-lookup"><span data-stu-id="9d952-115">'T</span></span>

<span data-ttu-id="9d952-116">Het type van elk element van `array` .</span><span class="sxs-lookup"><span data-stu-id="9d952-116">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d952-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9d952-117">See Also</span></span>

- [<span data-ttu-id="9d952-118">Micro soft. Quantum. arrays. SquareArrayFact</span><span class="sxs-lookup"><span data-stu-id="9d952-118">Microsoft.Quantum.Arrays.SquareArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.SquareArrayFact)