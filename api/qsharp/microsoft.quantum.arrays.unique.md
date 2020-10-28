---
uid: Microsoft.Quantum.Arrays.Unique
title: Unieke functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: c5d40bb82f2de640e9c78eef0c27e4766b477826
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705717"
---
# <a name="unique-function"></a><span data-ttu-id="dec9a-102">Unieke functie</span><span class="sxs-lookup"><span data-stu-id="dec9a-102">Unique function</span></span>

<span data-ttu-id="dec9a-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="dec9a-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="dec9a-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dec9a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dec9a-105">Retourneert een nieuwe matrix die geen gelijk aan aangrenzende elementen heeft.</span><span class="sxs-lookup"><span data-stu-id="dec9a-105">Returns a new array that has no equal adjacent elements.</span></span>

```qsharp
function Unique<'T> (equal : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="dec9a-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="dec9a-106">Description</span></span>

<span data-ttu-id="dec9a-107">Op basis van een aantal elementen en een functie om gelijkheid te testen, retourneert deze functie een nieuwe matrix waarin de relatieve volg orde van elementen wordt behouden, maar alle aangrenzende elementen die gelijk zijn, worden gefilterd op slechts één element.</span><span class="sxs-lookup"><span data-stu-id="dec9a-107">Given some array of elements and a function to test equality, this function returns a new array in which the relative order of elements is kept, but all adjacent elements which are equal are filtered to just a single element.</span></span>

## <a name="input"></a><span data-ttu-id="dec9a-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="dec9a-108">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="dec9a-109">gelijk aan: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="dec9a-109">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="dec9a-110">Een functie waarmee twee elementen worden vergeleken, zoals die worden `a` beschouwd als gelijk aan `b` `equal(a, b)` `true` .</span><span class="sxs-lookup"><span data-stu-id="dec9a-110">A function that compares two elements such that `a` is considered to be equal to `b` if `equal(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="dec9a-111">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="dec9a-111">array : 'T[]</span></span>

<span data-ttu-id="dec9a-112">De matrix die moet worden gefilterd op unieke elementen.</span><span class="sxs-lookup"><span data-stu-id="dec9a-112">The array to be filtered for unique elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="dec9a-113">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="dec9a-113">Output : 'T[]</span></span>

<span data-ttu-id="dec9a-114">Matrix zonder gelijke aangrenzende elementen.</span><span class="sxs-lookup"><span data-stu-id="dec9a-114">Array with no equal adjacent elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="dec9a-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="dec9a-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dec9a-116">T</span><span class="sxs-lookup"><span data-stu-id="dec9a-116">'T</span></span>

<span data-ttu-id="dec9a-117">Het type van elk element van `array` .</span><span class="sxs-lookup"><span data-stu-id="dec9a-117">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="dec9a-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="dec9a-118">Remarks</span></span>

<span data-ttu-id="dec9a-119">Als er meerdere elementen zijn die gelijk zijn, maar niet naast elkaar staan, worden er meerdere exemplaren in de uitvoer matrix weer.</span><span class="sxs-lookup"><span data-stu-id="dec9a-119">If there are multiple elements that are equal but not next to each other, there will be multiple occurrences in the output array.</span></span>  <span data-ttu-id="dec9a-120">Gebruik deze functie samen met `Sorted` om een matrix met algemene unieke elementen op te halen.</span><span class="sxs-lookup"><span data-stu-id="dec9a-120">Use this function together with `Sorted` to get an array with overall unique elements.</span></span>