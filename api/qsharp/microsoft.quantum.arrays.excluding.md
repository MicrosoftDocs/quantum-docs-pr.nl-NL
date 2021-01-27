---
uid: Microsoft.Quantum.Arrays.Excluding
title: Functie uitsluiten
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Excluding
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: c117431e3d98bba4ed3d29cb0b171247bf77be0b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848656"
---
# <a name="excluding-function"></a><span data-ttu-id="032ba-102">Functie uitsluiten</span><span class="sxs-lookup"><span data-stu-id="032ba-102">Excluding function</span></span>

<span data-ttu-id="032ba-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="032ba-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="032ba-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="032ba-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="032ba-105">Retourneert een matrix met de elementen van een andere matrix, met uitzonde ring van elementen in een bepaalde lijst met indices.</span><span class="sxs-lookup"><span data-stu-id="032ba-105">Returns an array containing the elements of another array, excluding elements at a given list of indices.</span></span>

```qsharp
function Excluding<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="032ba-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="032ba-106">Input</span></span>

### <a name="remove--int"></a><span data-ttu-id="032ba-107">verwijderen: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="032ba-107">remove : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="032ba-108">Een matrix met indices die aangeeft welke elementen moeten worden uitgesloten van de uitvoer.</span><span class="sxs-lookup"><span data-stu-id="032ba-108">An array of indices denoting which elements should be excluded from the output.</span></span>


### <a name="array--t"></a><span data-ttu-id="032ba-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="032ba-109">array : 'T[]</span></span>

<span data-ttu-id="032ba-110">Matrix waarvan de waarden in de uitvoer matrix worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="032ba-110">Array of which the values in the output array are taken.</span></span>



## <a name="output--t"></a><span data-ttu-id="032ba-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="032ba-111">Output : 'T[]</span></span>

<span data-ttu-id="032ba-112">Een matrix `output` , bijvoorbeeld `output[0]` het eerste element van `array` waarvan de index niet wordt weer gegeven `remove` , zoals `output[1]` de tweede elementen, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="032ba-112">An array `output` such that `output[0]` is the first element of `array` whose index does not appear in `remove`, such that `output[1]` is the second such element, and so forth.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="032ba-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="032ba-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="032ba-114">T</span><span class="sxs-lookup"><span data-stu-id="032ba-114">'T</span></span>

<span data-ttu-id="032ba-115">Het type van de matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="032ba-115">The type of the array elements.</span></span>

## <a name="example"></a><span data-ttu-id="032ba-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="032ba-116">Example</span></span>

```qsharp
let array = [10, 11, 12, 13, 14, 15];
// The following line returns [10, 12, 15].
let subarray = Excluding([1, 3, 4], array);
```