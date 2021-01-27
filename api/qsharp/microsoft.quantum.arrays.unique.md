---
uid: Microsoft.Quantum.Arrays.Unique
title: Unieke functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: b3aa03d20195bdd8bb64783a9b68cafac29e68f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850911"
---
# <a name="unique-function"></a><span data-ttu-id="5cb2c-102">Unieke functie</span><span class="sxs-lookup"><span data-stu-id="5cb2c-102">Unique function</span></span>

<span data-ttu-id="5cb2c-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="5cb2c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="5cb2c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5cb2c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5cb2c-105">Retourneert een nieuwe matrix die geen gelijk aan aangrenzende elementen heeft.</span><span class="sxs-lookup"><span data-stu-id="5cb2c-105">Returns a new array that has no equal adjacent elements.</span></span>

```qsharp
function Unique<'T> (equal : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="5cb2c-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="5cb2c-106">Description</span></span>

<span data-ttu-id="5cb2c-107">Op basis van een aantal elementen en een functie om gelijkheid te testen, retourneert deze functie een nieuwe matrix waarin de relatieve volg orde van elementen wordt behouden, maar alle aangrenzende elementen die gelijk zijn, worden gefilterd op slechts één element.</span><span class="sxs-lookup"><span data-stu-id="5cb2c-107">Given some array of elements and a function to test equality, this function returns a new array in which the relative order of elements is kept, but all adjacent elements which are equal are filtered to just a single element.</span></span>

## <a name="input"></a><span data-ttu-id="5cb2c-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="5cb2c-108">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="5cb2c-109">gelijk aan: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="5cb2c-109">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="5cb2c-110">Een functie waarmee twee elementen worden vergeleken, zoals die worden `a` beschouwd als gelijk aan `b` `equal(a, b)` `true` .</span><span class="sxs-lookup"><span data-stu-id="5cb2c-110">A function that compares two elements such that `a` is considered to be equal to `b` if `equal(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="5cb2c-111">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="5cb2c-111">array : 'T[]</span></span>

<span data-ttu-id="5cb2c-112">De matrix die moet worden gefilterd op unieke elementen.</span><span class="sxs-lookup"><span data-stu-id="5cb2c-112">The array to be filtered for unique elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="5cb2c-113">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="5cb2c-113">Output : 'T[]</span></span>

<span data-ttu-id="5cb2c-114">Matrix zonder gelijke aangrenzende elementen.</span><span class="sxs-lookup"><span data-stu-id="5cb2c-114">Array with no equal adjacent elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="5cb2c-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="5cb2c-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5cb2c-116">T</span><span class="sxs-lookup"><span data-stu-id="5cb2c-116">'T</span></span>

<span data-ttu-id="5cb2c-117">Het type van elk element van `array` .</span><span class="sxs-lookup"><span data-stu-id="5cb2c-117">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="5cb2c-118">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="5cb2c-118">Example</span></span>

```qsharp
let unique1 = Unique(EqualI, [1, 1, 3, 3, 2, 5, 5, 5, 7]);
// same as [1, 3, 2, 5, 7]
let unique2 = Unique(EqualI, [2, 2, 1, 1, 2, 2, 1, 1]);
// same as [2, 1, 2, 1];
let unique3 = Unique(EqualI, Sorted(LessThanOrEqualI, [2, 2, 1, 1, 2, 2, 1, 1]));
// same as [1, 2];
```

## <a name="remarks"></a><span data-ttu-id="5cb2c-119">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="5cb2c-119">Remarks</span></span>

<span data-ttu-id="5cb2c-120">Als er meerdere elementen zijn die gelijk zijn, maar niet naast elkaar staan, worden er meerdere exemplaren in de uitvoer matrix weer.</span><span class="sxs-lookup"><span data-stu-id="5cb2c-120">If there are multiple elements that are equal but not next to each other, there will be multiple occurrences in the output array.</span></span>  <span data-ttu-id="5cb2c-121">Gebruik deze functie samen met `Sorted` om een matrix met algemene unieke elementen op te halen.</span><span class="sxs-lookup"><span data-stu-id="5cb2c-121">Use this function together with `Sorted` to get an array with overall unique elements.</span></span>