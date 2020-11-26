---
uid: Microsoft.Quantum.Arrays.Filtered
title: Gefilterde functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Filtered
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: fa8600f4d773daf6eabf8b9961ab46961155d1fd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221263"
---
# <a name="filtered-function"></a><span data-ttu-id="3a9d4-102">Gefilterde functie</span><span class="sxs-lookup"><span data-stu-id="3a9d4-102">Filtered function</span></span>

<span data-ttu-id="3a9d4-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3a9d4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3a9d4-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3a9d4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3a9d4-105">Op basis van een matrix en een predikaat die is gedefinieerd voor de elementen van de matrix, retourneert een matrix die bestaat uit die elementen die voldoen aan het predicaat.</span><span class="sxs-lookup"><span data-stu-id="3a9d4-105">Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Filtered<'T> (predicate : ('T -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="3a9d4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="3a9d4-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="3a9d4-107">predikaat: niet-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3a9d4-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3a9d4-108">Een functie van `'T` naar een Booleaanse waarde die wordt gebruikt voor het filteren van elementen.</span><span class="sxs-lookup"><span data-stu-id="3a9d4-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="3a9d4-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="3a9d4-109">array : 'T[]</span></span>

<span data-ttu-id="3a9d4-110">Een matrix van elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="3a9d4-110">An array of elements over `'T`.</span></span>



## <a name="output--t"></a><span data-ttu-id="3a9d4-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="3a9d4-111">Output : 'T[]</span></span>

<span data-ttu-id="3a9d4-112">Een matrix `'T[]` met elementen die voldoen aan het predicaat.</span><span class="sxs-lookup"><span data-stu-id="3a9d4-112">An array `'T[]` of elements that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3a9d4-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="3a9d4-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3a9d4-114">T</span><span class="sxs-lookup"><span data-stu-id="3a9d4-114">'T</span></span>

<span data-ttu-id="3a9d4-115">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="3a9d4-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a9d4-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="3a9d4-116">Remarks</span></span>

<span data-ttu-id="3a9d4-117">De functie is gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix `'T[]` en een predikaat hebben waarop `'T -> Bool` we elementen kunnen filteren.</span><span class="sxs-lookup"><span data-stu-id="3a9d4-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>