---
uid: Microsoft.Quantum.Arrays.Unique
title: Unieke functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: 7964d5d41eb68cb05f9414164d69496c1f76eb08
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220005"
---
# <a name="unique-function"></a><span data-ttu-id="007f7-102">Unieke functie</span><span class="sxs-lookup"><span data-stu-id="007f7-102">Unique function</span></span>

<span data-ttu-id="007f7-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="007f7-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="007f7-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="007f7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="007f7-105">Retourneert een nieuwe matrix die geen gelijk aan aangrenzende elementen heeft.</span><span class="sxs-lookup"><span data-stu-id="007f7-105">Returns a new array that has no equal adjacent elements.</span></span>

```qsharp
function Unique<'T> (equal : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="007f7-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="007f7-106">Description</span></span>

<span data-ttu-id="007f7-107">Op basis van een aantal elementen en een functie om gelijkheid te testen, retourneert deze functie een nieuwe matrix waarin de relatieve volg orde van elementen wordt behouden, maar alle aangrenzende elementen die gelijk zijn, worden gefilterd op slechts één element.</span><span class="sxs-lookup"><span data-stu-id="007f7-107">Given some array of elements and a function to test equality, this function returns a new array in which the relative order of elements is kept, but all adjacent elements which are equal are filtered to just a single element.</span></span>

## <a name="input"></a><span data-ttu-id="007f7-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="007f7-108">Input</span></span>

### <a name="equal--tt---bool"></a><span data-ttu-id="007f7-109">gelijk aan: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="007f7-109">equal : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="007f7-110">Een functie waarmee twee elementen worden vergeleken, zoals die worden `a` beschouwd als gelijk aan `b` `equal(a, b)` `true` .</span><span class="sxs-lookup"><span data-stu-id="007f7-110">A function that compares two elements such that `a` is considered to be equal to `b` if `equal(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="007f7-111">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="007f7-111">array : 'T[]</span></span>

<span data-ttu-id="007f7-112">De matrix die moet worden gefilterd op unieke elementen.</span><span class="sxs-lookup"><span data-stu-id="007f7-112">The array to be filtered for unique elements.</span></span>



## <a name="output--t"></a><span data-ttu-id="007f7-113">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="007f7-113">Output : 'T[]</span></span>

<span data-ttu-id="007f7-114">Matrix zonder gelijke aangrenzende elementen.</span><span class="sxs-lookup"><span data-stu-id="007f7-114">Array with no equal adjacent elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="007f7-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="007f7-115">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="007f7-116">T</span><span class="sxs-lookup"><span data-stu-id="007f7-116">'T</span></span>

<span data-ttu-id="007f7-117">Het type van elk element van `array` .</span><span class="sxs-lookup"><span data-stu-id="007f7-117">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="007f7-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="007f7-118">Remarks</span></span>

<span data-ttu-id="007f7-119">Als er meerdere elementen zijn die gelijk zijn, maar niet naast elkaar staan, worden er meerdere exemplaren in de uitvoer matrix weer.</span><span class="sxs-lookup"><span data-stu-id="007f7-119">If there are multiple elements that are equal but not next to each other, there will be multiple occurrences in the output array.</span></span>  <span data-ttu-id="007f7-120">Gebruik deze functie samen met `Sorted` om een matrix met algemene unieke elementen op te halen.</span><span class="sxs-lookup"><span data-stu-id="007f7-120">Use this function together with `Sorted` to get an array with overall unique elements.</span></span>