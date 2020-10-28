---
uid: Microsoft.Quantum.Arrays.Count
title: Functie Count
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Count
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 408a4a42dda6a4827db6d5865e2b4b8a8df5b37a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706132"
---
# <a name="count-function"></a><span data-ttu-id="fc64a-102">Functie Count</span><span class="sxs-lookup"><span data-stu-id="fc64a-102">Count function</span></span>

<span data-ttu-id="fc64a-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="fc64a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="fc64a-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fc64a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fc64a-105">Op basis van een matrix en een predikaat die is gedefinieerd voor de elementen van de matrix, retourneert het aantal elementen een matrix die bestaat uit die elementen die voldoen aan het predicaat.</span><span class="sxs-lookup"><span data-stu-id="fc64a-105">Given an array and a predicate that is defined for the elements of the array, returns the number of elements an array that consists of those elements that satisfy the predicate.</span></span>

```qsharp
function Count<'T> (predicate : ('T -> Bool), array : 'T[]) : Int
```


## <a name="input"></a><span data-ttu-id="fc64a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="fc64a-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="fc64a-107">predikaat: niet-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="fc64a-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="fc64a-108">Een functie van `'T` naar een Booleaanse waarde die wordt gebruikt voor het filteren van elementen.</span><span class="sxs-lookup"><span data-stu-id="fc64a-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="fc64a-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="fc64a-109">array : 'T[]</span></span>

<span data-ttu-id="fc64a-110">Een matrix van elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="fc64a-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="fc64a-111">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fc64a-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fc64a-112">Het aantal elementen in `array` dat voldoet aan het predicaat.</span><span class="sxs-lookup"><span data-stu-id="fc64a-112">The number of elements in `array` that satisfy the predicate.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fc64a-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="fc64a-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fc64a-114">T</span><span class="sxs-lookup"><span data-stu-id="fc64a-114">'T</span></span>

<span data-ttu-id="fc64a-115">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="fc64a-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc64a-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="fc64a-116">Remarks</span></span>

<span data-ttu-id="fc64a-117">De functie is gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix `'T[]` en een predikaat hebben waarop `'T -> Bool` we elementen kunnen filteren.</span><span class="sxs-lookup"><span data-stu-id="fc64a-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a predicate `'T -> Bool` we can filter elements.</span></span>