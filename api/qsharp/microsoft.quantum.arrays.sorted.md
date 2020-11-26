---
uid: Microsoft.Quantum.Arrays.Sorted
title: Functie gesorteerd
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Sorted
qsharp.summary: Given an array, returns the elements of that array sorted by a given comparison function.
ms.openlocfilehash: bd8b869e03c7f4687c456a944e07a811ae0d2ce2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220226"
---
# <a name="sorted-function"></a><span data-ttu-id="eff40-102">Functie gesorteerd</span><span class="sxs-lookup"><span data-stu-id="eff40-102">Sorted function</span></span>

<span data-ttu-id="eff40-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="eff40-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="eff40-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="eff40-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="eff40-105">Op basis van een matrix retourneert de elementen van die matrix, gesorteerd op een bepaalde vergelijkings functie.</span><span class="sxs-lookup"><span data-stu-id="eff40-105">Given an array, returns the elements of that array sorted by a given comparison function.</span></span>

```qsharp
function Sorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="eff40-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="eff40-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="eff40-107">vergelijking: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="eff40-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="eff40-108">Een functie die twee elementen vergelijkt, zodat deze `a` kleiner is dan of gelijk is aan `b` if `comparison(a, b)` `true` .</span><span class="sxs-lookup"><span data-stu-id="eff40-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="eff40-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="eff40-109">array : 'T[]</span></span>

<span data-ttu-id="eff40-110">De matrix die moet worden gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="eff40-110">The array to be sorted.</span></span>



## <a name="output--t"></a><span data-ttu-id="eff40-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="eff40-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="eff40-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="eff40-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="eff40-113">T</span><span class="sxs-lookup"><span data-stu-id="eff40-113">'T</span></span>

<span data-ttu-id="eff40-114">Het type van elk element van `array` .</span><span class="sxs-lookup"><span data-stu-id="eff40-114">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="eff40-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="eff40-115">Remarks</span></span>

<span data-ttu-id="eff40-116">Er `comparison` wordt van uitgegaan dat de functie transitief is, bijvoorbeeld als `comparison(a, b)` en `comparison(b, c)` `comparison(a, c)` wordt aangenomen.</span><span class="sxs-lookup"><span data-stu-id="eff40-116">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="eff40-117">Als deze eigenschap niet in de wachtrij staat, is de uitvoer van deze functie mogelijk onjuist.</span><span class="sxs-lookup"><span data-stu-id="eff40-117">If this property does not hold, then the output of this function may be incorrect.</span></span>

<span data-ttu-id="eff40-118">Aangezien dit een functie is, zijn de resultaten volledig determinstic, zelfs wanneer twee elementen worden beschouwd als gelijk onder `comparison` ; dat wil zeggen, wanneer `comparison(a, b)` en `comparison(b, a)` beide `true` .</span><span class="sxs-lookup"><span data-stu-id="eff40-118">As this is a function, the results are completely determinstic, even when two elements are considered equal under `comparison`; that is, when `comparison(a, b)` and `comparison(b, a)` are both `true`.</span></span>
<span data-ttu-id="eff40-119">Met name de sorteer bewerking die door deze functie wordt uitgevoerd, is gegarandeerd stabiel, zodat er twee elementen `a` `b` in die volg orde worden `array` weer gegeven en worden beschouwd als gelijk onder `comparison` `a` . deze worden ook voor `b` in de uitvoer opgenomen.</span><span class="sxs-lookup"><span data-stu-id="eff40-119">In particular, the sort performed by this function is guaranteed to be stable, so that if two elements `a` and `b` occur in that order within `array` and are considered equal under `comparison`, then `a` will also appear before `b` in the output.</span></span>

<span data-ttu-id="eff40-120">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="eff40-120">For example:</span></span>

```Q#
function LastDigitLessThanOrEqual(left : Int, right : Int) : Bool {
    return LessThanOrEqualI(
        left % 10, right % 10
    );
}

function SortedByLastDigit() : Int[] {
    return Sorted(LastDigitLessThanOrEqual, [3, 37, 11, 17]);
}
// returns [11, 3, 37, 17].
```