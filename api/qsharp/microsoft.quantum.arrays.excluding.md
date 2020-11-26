---
uid: Microsoft.Quantum.Arrays.Excluding
title: Functie uitsluiten
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Excluding
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: 6585e619834a96953c9eae2d36a8ebe0a11dbda0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221314"
---
# <a name="excluding-function"></a><span data-ttu-id="0b052-102">Functie uitsluiten</span><span class="sxs-lookup"><span data-stu-id="0b052-102">Excluding function</span></span>

<span data-ttu-id="0b052-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="0b052-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="0b052-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0b052-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0b052-105">Retourneert een matrix met de elementen van een andere matrix, met uitzonde ring van elementen in een bepaalde lijst met indices.</span><span class="sxs-lookup"><span data-stu-id="0b052-105">Returns an array containing the elements of another array, excluding elements at a given list of indices.</span></span>

```qsharp
function Excluding<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="0b052-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="0b052-106">Input</span></span>

### <a name="remove--int"></a><span data-ttu-id="0b052-107">verwijderen: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="0b052-107">remove : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="0b052-108">Een matrix met indices die aangeeft welke elementen moeten worden uitgesloten van de uitvoer.</span><span class="sxs-lookup"><span data-stu-id="0b052-108">An array of indices denoting which elements should be excluded from the output.</span></span>


### <a name="array--t"></a><span data-ttu-id="0b052-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="0b052-109">array : 'T[]</span></span>

<span data-ttu-id="0b052-110">Matrix waarvan de waarden in de uitvoer matrix worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="0b052-110">Array of which the values in the output array are taken.</span></span>



## <a name="output--t"></a><span data-ttu-id="0b052-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="0b052-111">Output : 'T[]</span></span>

<span data-ttu-id="0b052-112">Een matrix `output` , bijvoorbeeld `output[0]` het eerste element van `array` waarvan de index niet wordt weer gegeven `remove` , zoals `output[1]` de tweede elementen, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="0b052-112">An array `output` such that `output[0]` is the first element of `array` whose index does not appear in `remove`, such that `output[1]` is the second such element, and so forth.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="0b052-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="0b052-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="0b052-114">T</span><span class="sxs-lookup"><span data-stu-id="0b052-114">'T</span></span>

<span data-ttu-id="0b052-115">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="0b052-115">The type of the array elements.</span></span>