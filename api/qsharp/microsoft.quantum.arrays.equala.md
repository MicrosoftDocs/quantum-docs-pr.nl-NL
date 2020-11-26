---
uid: Microsoft.Quantum.Arrays.EqualA
title: De functie equals
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EqualA
qsharp.summary: Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.
ms.openlocfilehash: 176e15139a27d375fb047c07fa1ee778dc8cc2ce
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221365"
---
# <a name="equala-function"></a><span data-ttu-id="3c91d-102">De functie equals</span><span class="sxs-lookup"><span data-stu-id="3c91d-102">EqualA function</span></span>

<span data-ttu-id="3c91d-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3c91d-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3c91d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3c91d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3c91d-105">Op basis van twee matrices van hetzelfde type en een predikaat dat is gedefinieerd voor paren van elementen van de matrices, wordt gecontroleerd of de matrices gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="3c91d-105">Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.</span></span>

```qsharp
function EqualA<'T> (equal : (('T, 'T) -> Bool), array1 : 'T[], array2 : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="3c91d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="3c91d-106">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="3c91d-107">gelijk aan: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3c91d-107">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3c91d-108">Een functie van tuple `('T, 'T)` naar `Bool` die wordt gebruikt om te controleren of twee elementen van matrices gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="3c91d-108">A function from tuple `('T, 'T)` to `Bool` that is used to check whether two elements of arrays are equal.</span></span>


### <a name="array1--t"></a><span data-ttu-id="3c91d-109">matrix1: 'T []</span><span class="sxs-lookup"><span data-stu-id="3c91d-109">array1 : 'T[]</span></span>

<span data-ttu-id="3c91d-110">De eerste matrix die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="3c91d-110">The first array to be compared.</span></span>


### <a name="array2--t"></a><span data-ttu-id="3c91d-111">matrix2: ' []</span><span class="sxs-lookup"><span data-stu-id="3c91d-111">array2 : 'T[]</span></span>

<span data-ttu-id="3c91d-112">De tweede matrix die moet worden vergeleken.</span><span class="sxs-lookup"><span data-stu-id="3c91d-112">The second array to be compared.</span></span>



## <a name="output--bool"></a><span data-ttu-id="3c91d-113">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="3c91d-113">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="3c91d-114">De waarde `true` als en alleen als `array1` en `array2` gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="3c91d-114">The value `true` if and only if `array1` and `array2` are equal.</span></span>
<span data-ttu-id="3c91d-115">Dat wil zeggen, als beide matrices dezelfde lengte hebben en alle elementen gelijk zijn aan zoals gedefinieerd door `equal` .</span><span class="sxs-lookup"><span data-stu-id="3c91d-115">That is, if both arrays have the same length, and all elements are equal as defined by `equal`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3c91d-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="3c91d-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3c91d-117">T</span><span class="sxs-lookup"><span data-stu-id="3c91d-117">'T</span></span>

<span data-ttu-id="3c91d-118">Het type van de elementen van elke matrix.</span><span class="sxs-lookup"><span data-stu-id="3c91d-118">The type of each array's elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c91d-119">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="3c91d-119">Remarks</span></span>

<span data-ttu-id="3c91d-120">Deze functie is gedefinieerd voor algemene typen. Wanneer we twee matrices `'T[]` en een functie hebben `equal: ('T, 'T) -> Bool` , retourneert deze functie dus een `Bool` waarde die aangeeft of de matrices gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="3c91d-120">This function is defined for generic types; i.e., whenever we have two arrays `'T[]` and a function `equal: ('T, 'T) -> Bool`, this function returns a `Bool` value that indicates whether the arrays are equal.</span></span>
<span data-ttu-id="3c91d-121">Als twee matrices als gelijk moeten worden beschouwd, moeten ze dezelfde lengte hebben en moeten de elementen in dezelfde posities in de matrices gelijk zijn.</span><span class="sxs-lookup"><span data-stu-id="3c91d-121">For two arrays to be considered equal, they have to have equal length and the elements in the same positions in the arrays have to be equal.</span></span>