---
uid: Microsoft.Quantum.Arrays.Exclude
title: De functie exclude
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Exclude
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: e1fa7e728d4846db90872055454a8182a77a518b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706052"
---
# <a name="exclude-function"></a><span data-ttu-id="40f3e-102">De functie exclude</span><span class="sxs-lookup"><span data-stu-id="40f3e-102">Exclude function</span></span>

<span data-ttu-id="40f3e-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="40f3e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="40f3e-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="40f3e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="40f3e-105">Retourneert een matrix met de elementen van een andere matrix, met uitzonde ring van elementen in een bepaalde lijst met indices.</span><span class="sxs-lookup"><span data-stu-id="40f3e-105">Returns an array containing the elements of another array, excluding elements at a given list of indices.</span></span>

```qsharp
function Exclude<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="40f3e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="40f3e-106">Input</span></span>

### <a name="remove--int"></a><span data-ttu-id="40f3e-107">verwijderen: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="40f3e-107">remove : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="40f3e-108">Een matrix met indices die aangeeft welke elementen moeten worden uitgesloten van de uitvoer.</span><span class="sxs-lookup"><span data-stu-id="40f3e-108">An array of indices denoting which elements should be excluded from the output.</span></span>


### <a name="array--t"></a><span data-ttu-id="40f3e-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="40f3e-109">array : 'T[]</span></span>

<span data-ttu-id="40f3e-110">Matrix waarvan de waarden in de uitvoer matrix worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="40f3e-110">Array of which the values in the output array are taken.</span></span>



## <a name="output--t"></a><span data-ttu-id="40f3e-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="40f3e-111">Output : 'T[]</span></span>

<span data-ttu-id="40f3e-112">Een matrix `output` , bijvoorbeeld `output[0]` het eerste element van `array` waarvan de index niet wordt weer gegeven `remove` , zoals `output[1]` de tweede elementen, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="40f3e-112">An array `output` such that `output[0]` is the first element of `array` whose index does not appear in `remove`, such that `output[1]` is the second such element, and so forth.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="40f3e-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="40f3e-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="40f3e-114">T</span><span class="sxs-lookup"><span data-stu-id="40f3e-114">'T</span></span>

<span data-ttu-id="40f3e-115">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="40f3e-115">The type of the array elements.</span></span>