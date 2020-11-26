---
uid: Microsoft.Quantum.Arrays.SquareArrayFact
title: De functie SquareArrayFact
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SquareArrayFact
qsharp.summary: Represents a condition that a 2-dimensional array has a square shape
ms.openlocfilehash: 3529718f0c903266d21fd593c11c0149dae0fa2c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220192"
---
# <a name="squarearrayfact-function"></a><span data-ttu-id="81d58-102">De functie SquareArrayFact</span><span class="sxs-lookup"><span data-stu-id="81d58-102">SquareArrayFact function</span></span>

<span data-ttu-id="81d58-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="81d58-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="81d58-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="81d58-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="81d58-105">Vertegenwoordigt een voor waarde dat een tweedimensionale matrix een vier Kante vorm heeft</span><span class="sxs-lookup"><span data-stu-id="81d58-105">Represents a condition that a 2-dimensional array has a square shape</span></span>

```qsharp
function SquareArrayFact<'T> (array : 'T[][], message : String) : Unit
```


## <a name="description"></a><span data-ttu-id="81d58-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="81d58-106">Description</span></span>

<span data-ttu-id="81d58-107">Deze functie beweringt dat elke rij in een matrix net zoveel elementen bevat als er rijen (elementen) in de matrix zijn.</span><span class="sxs-lookup"><span data-stu-id="81d58-107">This function asserts that each row in an array has as many elements as there are rows (elements) in the array.</span></span>

## <a name="input"></a><span data-ttu-id="81d58-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="81d58-108">Input</span></span>

### <a name="array--t"></a><span data-ttu-id="81d58-109">matrix: ' [] []</span><span class="sxs-lookup"><span data-stu-id="81d58-109">array : 'T[][]</span></span>

<span data-ttu-id="81d58-110">Een 2-dimensionale matrix van elementen</span><span class="sxs-lookup"><span data-stu-id="81d58-110">A 2-dimensional array of elements</span></span>


### <a name="message--string"></a><span data-ttu-id="81d58-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="81d58-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="81d58-112">Een bericht dat moet worden afgedrukt als de matrix geen vier Kante matrix is</span><span class="sxs-lookup"><span data-stu-id="81d58-112">A message to be printed if the array is not a square array</span></span>



## <a name="output--unit"></a><span data-ttu-id="81d58-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="81d58-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="81d58-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="81d58-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="81d58-115">T</span><span class="sxs-lookup"><span data-stu-id="81d58-115">'T</span></span>

<span data-ttu-id="81d58-116">Het type van elk element van `array` .</span><span class="sxs-lookup"><span data-stu-id="81d58-116">The type of each element of `array`.</span></span>

## <a name="see-also"></a><span data-ttu-id="81d58-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="81d58-117">See Also</span></span>

- [<span data-ttu-id="81d58-118">Micro soft. Quantum. arrays. RectangularArrayFact</span><span class="sxs-lookup"><span data-stu-id="81d58-118">Microsoft.Quantum.Arrays.RectangularArrayFact</span></span>](xref:Microsoft.Quantum.Arrays.RectangularArrayFact)