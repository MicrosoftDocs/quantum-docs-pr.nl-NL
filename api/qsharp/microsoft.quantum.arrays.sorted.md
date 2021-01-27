---
uid: Microsoft.Quantum.Arrays.Sorted
title: Functie gesorteerd
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Sorted
qsharp.summary: Given an array, returns the elements of that array sorted by a given comparison function.
ms.openlocfilehash: cb8a1ef438d798c8201ed9f52677e253770df1d3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845443"
---
# <a name="sorted-function"></a><span data-ttu-id="d9dce-102">Functie gesorteerd</span><span class="sxs-lookup"><span data-stu-id="d9dce-102">Sorted function</span></span>

<span data-ttu-id="d9dce-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d9dce-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d9dce-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d9dce-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d9dce-105">Op basis van een matrix retourneert de elementen van die matrix, gesorteerd op een bepaalde vergelijkings functie.</span><span class="sxs-lookup"><span data-stu-id="d9dce-105">Given an array, returns the elements of that array sorted by a given comparison function.</span></span>

```qsharp
function Sorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="d9dce-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d9dce-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="d9dce-107">vergelijking: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="d9dce-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="d9dce-108">Een functie die twee elementen vergelijkt, zodat deze `a` kleiner is dan of gelijk is aan `b` if `comparison(a, b)` `true` .</span><span class="sxs-lookup"><span data-stu-id="d9dce-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="d9dce-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="d9dce-109">array : 'T[]</span></span>

<span data-ttu-id="d9dce-110">De matrix die moet worden gesorteerd.</span><span class="sxs-lookup"><span data-stu-id="d9dce-110">The array to be sorted.</span></span>



## <a name="output--t"></a><span data-ttu-id="d9dce-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="d9dce-111">Output : 'T[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d9dce-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d9dce-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d9dce-113">T</span><span class="sxs-lookup"><span data-stu-id="d9dce-113">'T</span></span>

<span data-ttu-id="d9dce-114">Het type van elk element van `array` .</span><span class="sxs-lookup"><span data-stu-id="d9dce-114">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="d9dce-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="d9dce-115">Example</span></span>

<span data-ttu-id="d9dce-116">In het volgende fragment wordt een matrix met gehele getallen gesorteerd die in oplopende volg orde moet worden uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="d9dce-116">The following snippet sorts an array of integers to occur in ascending order:</span></span>

```qsharp
let sortedArray = Sorted(LessThanOrEqualI, [3, 17, 11, -201, -11]);
```

## <a name="remarks"></a><span data-ttu-id="d9dce-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d9dce-117">Remarks</span></span>

<span data-ttu-id="d9dce-118">Er `comparison` wordt van uitgegaan dat de functie transitief is, bijvoorbeeld als `comparison(a, b)` en `comparison(b, c)` `comparison(a, c)` wordt aangenomen.</span><span class="sxs-lookup"><span data-stu-id="d9dce-118">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="d9dce-119">Als deze eigenschap niet in de wachtrij staat, is de uitvoer van deze functie mogelijk onjuist.</span><span class="sxs-lookup"><span data-stu-id="d9dce-119">If this property does not hold, then the output of this function may be incorrect.</span></span>

<span data-ttu-id="d9dce-120">Aangezien dit een functie is, zijn de resultaten volledig determinstic, zelfs wanneer twee elementen worden beschouwd als gelijk onder `comparison` ; dat wil zeggen, wanneer `comparison(a, b)` en `comparison(b, a)` beide `true` .</span><span class="sxs-lookup"><span data-stu-id="d9dce-120">As this is a function, the results are completely determinstic, even when two elements are considered equal under `comparison`; that is, when `comparison(a, b)` and `comparison(b, a)` are both `true`.</span></span>
<span data-ttu-id="d9dce-121">Met name de sorteer bewerking die door deze functie wordt uitgevoerd, is gegarandeerd stabiel, zodat er twee elementen `a` `b` in die volg orde worden `array` weer gegeven en worden beschouwd als gelijk onder `comparison` `a` . deze worden ook voor `b` in de uitvoer opgenomen.</span><span class="sxs-lookup"><span data-stu-id="d9dce-121">In particular, the sort performed by this function is guaranteed to be stable, so that if two elements `a` and `b` occur in that order within `array` and are considered equal under `comparison`, then `a` will also appear before `b` in the output.</span></span>

<span data-ttu-id="d9dce-122">Bijvoorbeeld:</span><span class="sxs-lookup"><span data-stu-id="d9dce-122">For example:</span></span>

```qsharp
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