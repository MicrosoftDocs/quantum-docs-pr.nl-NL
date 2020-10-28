---
uid: Microsoft.Quantum.Arrays.EqualA
title: De functie equals
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EqualA
qsharp.summary: Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.
ms.openlocfilehash: 24fd76aaeb66081d6d8f1eaa3056117f54b5a5e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706053"
---
# <a name="equala-function"></a><span data-ttu-id="a8240-102">De functie equals</span><span class="sxs-lookup"><span data-stu-id="a8240-102">EqualA function</span></span>

<span data-ttu-id="a8240-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a8240-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a8240-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a8240-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a8240-105">Op basis van twee matrices van hetzelfde type en een predikaat dat is gedefinieerd voor paren van elementen van de matrices, wordt gecontroleerd of de matrices gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="a8240-105">Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.</span></span>

```qsharp
function EqualA<'T> (equal : (('T, 'T) -> Bool), array1 : 'T[], array2 : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="a8240-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a8240-106">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="a8240-107">gelijk aan: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a8240-107">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a8240-108">Een functie van tuple `('T, 'T)` naar `Bool` die wordt gebruikt om te controleren of twee elementen van matrices gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="a8240-108">A function from tuple `('T, 'T)` to `Bool` that is used to check whether two elements of arrays are equal.</span></span>


### <a name="array1--t"></a><span data-ttu-id="a8240-109">matrix1: 'T []</span><span class="sxs-lookup"><span data-stu-id="a8240-109">array1 : 'T[]</span></span>

<span data-ttu-id="a8240-110">De eerste matrix die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="a8240-110">The first array to be compared.</span></span>


### <a name="array2--t"></a><span data-ttu-id="a8240-111">matrix2: ' []</span><span class="sxs-lookup"><span data-stu-id="a8240-111">array2 : 'T[]</span></span>

<span data-ttu-id="a8240-112">De tweede matrix die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="a8240-112">The second array to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a8240-113">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a8240-113">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a8240-114">De waarde `true` als en alleen als `array1` en `array2` gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="a8240-114">The value `true` if and only if `array1` and `array2` are equal.</span></span>
<span data-ttu-id="a8240-115">Dat wil zeggen, als beide matrices dezelfde lengte hebben en alle elementen gelijk zijn aan zoals gedefinieerd door `equal` .</span><span class="sxs-lookup"><span data-stu-id="a8240-115">That is, if both arrays have the same length, and all elements are equal as defined by `equal`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a8240-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a8240-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a8240-117">T</span><span class="sxs-lookup"><span data-stu-id="a8240-117">'T</span></span>

<span data-ttu-id="a8240-118">Het type van de elementen van elke matrix.</span><span class="sxs-lookup"><span data-stu-id="a8240-118">The type of each array's elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8240-119">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="a8240-119">Remarks</span></span>

<span data-ttu-id="a8240-120">Deze functie is gedefinieerd voor algemene typen. Wanneer we twee matrices `'T[]` en een functie hebben `equal: ('T, 'T) -> Bool` , retourneert deze functie dus een `Bool` waarde die aangeeft of de matrices gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="a8240-120">This function is defined for generic types; i.e., whenever we have two arrays `'T[]` and a function `equal: ('T, 'T) -> Bool`, this function returns a `Bool` value that indicates whether the arrays are equal.</span></span>
<span data-ttu-id="a8240-121">Als twee matrices als gelijk moeten worden beschouwd, moeten ze dezelfde lengte hebben en moeten de elementen in dezelfde posities in de matrices gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="a8240-121">For two arrays to be considered equal, they have to have equal length and the elements in the same positions in the arrays have to be equal.</span></span>