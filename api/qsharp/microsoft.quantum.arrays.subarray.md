---
uid: Microsoft.Quantum.Arrays.Subarray
title: Submatrix functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Subarray
qsharp.summary: Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.
ms.openlocfilehash: ccc041da0213d1f5dc5c8b4ff7a03b8b01ad107d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845423"
---
# <a name="subarray-function"></a><span data-ttu-id="b8c2c-102">Submatrix functie</span><span class="sxs-lookup"><span data-stu-id="b8c2c-102">Subarray function</span></span>

<span data-ttu-id="b8c2c-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="b8c2c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="b8c2c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b8c2c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b8c2c-105">Neemt een matrix en een lijst met locaties en produceert een nieuwe matrix die is samengesteld op basis van de elementen van de oorspronkelijke matrix die overeenkomen met de opgegeven locaties.</span><span class="sxs-lookup"><span data-stu-id="b8c2c-105">Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.</span></span>

```qsharp
function Subarray<'T> (indices : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="b8c2c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b8c2c-106">Input</span></span>

### <a name="indices--int"></a><span data-ttu-id="b8c2c-107">indices: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="b8c2c-107">indices : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="b8c2c-108">Een lijst met gehele getallen die wordt gebruikt voor het definiëren van de submatrix.</span><span class="sxs-lookup"><span data-stu-id="b8c2c-108">A list of integers that is used to define the subarray.</span></span>


### <a name="array--t"></a><span data-ttu-id="b8c2c-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="b8c2c-109">array : 'T[]</span></span>

<span data-ttu-id="b8c2c-110">Een matrix van elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="b8c2c-110">An array of elements over `'T`.</span></span>



## <a name="output--t"></a><span data-ttu-id="b8c2c-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="b8c2c-111">Output : 'T[]</span></span>

<span data-ttu-id="b8c2c-112">Een matrix `out` met elementen waarvan de indices overeenkomen met de submatrix, dat wil zeggen `out[idx] == array[indices[idx]]` .</span><span class="sxs-lookup"><span data-stu-id="b8c2c-112">An array `out` of elements whose indices correspond to the subarray, such that `out[idx] == array[indices[idx]]`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b8c2c-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="b8c2c-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b8c2c-114">T</span><span class="sxs-lookup"><span data-stu-id="b8c2c-114">'T</span></span>

<span data-ttu-id="b8c2c-115">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="b8c2c-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8c2c-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="b8c2c-116">Remarks</span></span>

<span data-ttu-id="b8c2c-117">De functie is gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix hebben `'T[]` en een lijst met locaties `Int[]` waarmee de submatrix wordt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="b8c2c-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a list of locations `Int[]` defining the subarray.</span></span>
<span data-ttu-id="b8c2c-118">De constructie van de submatrix is een gebaseerd op het genereren van een nieuwe, diep gaande kopie van de opgegeven matrix in plaats van verwijzingen te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="b8c2c-118">The construction of the subarray is a based on generating a new, deep copy of the given array as opposed to maintaining references.</span></span>

<span data-ttu-id="b8c2c-119">Als `Length(indices) < Length(array)` deze functie een subset retourneert, wordt geretourneerd `array` .</span><span class="sxs-lookup"><span data-stu-id="b8c2c-119">If `Length(indices) < Length(array)`, this function will return a subset of `array`.</span></span> <span data-ttu-id="b8c2c-120">Als er daarentegen `indices` herhaalde elementen bevatten, worden ook de bijbehorende elementen van `array` herhaald.</span><span class="sxs-lookup"><span data-stu-id="b8c2c-120">On the other hand, if `indices` contains repeated elements, the corresponding elements of `array` will likewise be repeated.</span></span>
<span data-ttu-id="b8c2c-121">Als `indices` en `array` dezelfde lengte hebben, biedt deze functie permutaties van `array` .</span><span class="sxs-lookup"><span data-stu-id="b8c2c-121">If `indices` and `array` are the same length, this function provides permutations of `array`.</span></span>