---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: De functie SquareArrayFact
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: a154e5becba4dae762596a3fc1b268855520fa1b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850966"
---
# <a name="squarearrayfact-function"></a><span data-ttu-id="dfa8c-102">De functie SquareArrayFact</span><span class="sxs-lookup"><span data-stu-id="dfa8c-102">SquareArrayFact function</span></span>

<span data-ttu-id="dfa8c-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="dfa8c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="dfa8c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dfa8c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dfa8c-105">Vertegenwoordigt een voor waarde dat een tweedimensionale matrix een vier Kante vorm heeft</span><span class="sxs-lookup"><span data-stu-id="dfa8c-105">Represents a condition that a 2-dimensional array has a square shape</span></span>

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="dfa8c-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="dfa8c-106">Description</span></span>

<span data-ttu-id="dfa8c-107">Deze functie beweringt dat elke rij in een matrix net zoveel elementen bevat als er rijen (elementen) in de matrix zijn.</span><span class="sxs-lookup"><span data-stu-id="dfa8c-107">This function asserts that each row in an array has as many elements as there are rows (elements) in the array.</span></span>

## <a name="input"></a><span data-ttu-id="dfa8c-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="dfa8c-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="dfa8c-109">matrix: ' [] []</span><span class="sxs-lookup"><span data-stu-id="dfa8c-109">array : 'T[][]</span></span>

<span data-ttu-id="dfa8c-110">Een 2-dimensionale matrix van elementen</span><span class="sxs-lookup"><span data-stu-id="dfa8c-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="dfa8c-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="dfa8c-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="dfa8c-112">Een bericht dat moet worden afgedrukt als de matrix geen vier Kante matrix is</span><span class="sxs-lookup"><span data-stu-id="dfa8c-112">A message to be printed if the array is not a square array</span></span>



## <a name="output--unit"></a><span data-ttu-id="dfa8c-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dfa8c-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="dfa8c-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="dfa8c-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dfa8c-115">T</span><span class="sxs-lookup"><span data-stu-id="dfa8c-115">'T</span></span>

<span data-ttu-id="dfa8c-116">Het type van elk element van `array` .</span><span class="sxs-lookup"><span data-stu-id="dfa8c-116">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="dfa8c-117">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="dfa8c-117">Example</span></span>

```qsharp
SquareArrayFact([[1, 2], [3, 4]], "Array is not a square");       // okay
SquareArrayFact([[1, 2, 3], [4, 5, 6]], "Array is not a square"); // will fail
SquareArrayFact([[1, 2], [3, 4, 5]], "Array is not a square");    // will fail
```

## <a name="see-also"></a><span data-ttu-id="dfa8c-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="dfa8c-118">See Also</span></span>

- [<span data-ttu-id="dfa8c-119">Micro soft. Quantum. arrays. RectangularArrayFact</span><span class="sxs-lookup"><span data-stu-id="dfa8c-119">Microsoft.Quantum.Arrays.RectangularArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)