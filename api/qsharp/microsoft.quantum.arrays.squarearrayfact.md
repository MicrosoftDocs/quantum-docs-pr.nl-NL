---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: De functie SquareArrayFact
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: f7f0573db9098feebfd481624e11119c58fd9eed
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705765"
---
# <a name="squarearrayfact-function"></a><span data-ttu-id="37971-102">De functie SquareArrayFact</span><span class="sxs-lookup"><span data-stu-id="37971-102">SquareArrayFact function</span></span>

<span data-ttu-id="37971-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="37971-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="37971-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="37971-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="37971-105">Vertegenwoordigt een voor waarde dat een tweedimensionale matrix een vier Kante vorm heeft</span><span class="sxs-lookup"><span data-stu-id="37971-105">Represents a condition that a 2-dimensional array has a square shape</span></span>

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="37971-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="37971-106">Description</span></span>

<span data-ttu-id="37971-107">Deze functie beweringt dat elke rij in een matrix net zoveel elementen bevat als er rijen (elementen) in de matrix zijn.</span><span class="sxs-lookup"><span data-stu-id="37971-107">This function asserts that each row in an array has as many elements as there are rows (elements) in the array.</span></span>

## <a name="input"></a><span data-ttu-id="37971-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="37971-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="37971-109">matrix: ' [] []</span><span class="sxs-lookup"><span data-stu-id="37971-109">array : 'T[][]</span></span>

<span data-ttu-id="37971-110">Een 2-dimensionale matrix van elementen</span><span class="sxs-lookup"><span data-stu-id="37971-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="37971-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="37971-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="37971-112">Een bericht dat moet worden afgedrukt als de matrix geen vier Kante matrix is</span><span class="sxs-lookup"><span data-stu-id="37971-112">A message to be printed if the array is not a square array</span></span>



## <a name="output--unit"></a><span data-ttu-id="37971-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="37971-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="37971-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="37971-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="37971-115">T</span><span class="sxs-lookup"><span data-stu-id="37971-115">'T</span></span>

<span data-ttu-id="37971-116">Het type van elk element van `array` .</span><span class="sxs-lookup"><span data-stu-id="37971-116">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="37971-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="37971-117">See Also</span></span>

- [<span data-ttu-id="37971-118">Micro soft. Quantum. arrays. RectangularArrayFact</span><span class="sxs-lookup"><span data-stu-id="37971-118">Microsoft.Quantum.Arrays.RectangularArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)