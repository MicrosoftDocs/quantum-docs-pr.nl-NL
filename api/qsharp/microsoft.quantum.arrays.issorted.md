---
uid: Microsoft.Quantum.Arrays.IsSorted
title: De functie IsSorted
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsSorted
qsharp.summary: Given an array, returns whether that array is sorted as defined by a given comparison function.
ms.openlocfilehash: 330c1f789585f64cf255bc74f8a9c1ccf81b009e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705932"
---
# <a name="issorted-function"></a><span data-ttu-id="a161f-102">De functie IsSorted</span><span class="sxs-lookup"><span data-stu-id="a161f-102">IsSorted function</span></span>

<span data-ttu-id="a161f-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a161f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a161f-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a161f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a161f-105">Retourneert aan de hand van een matrix of die matrix is gesorteerd zoals gedefinieerd door een bepaalde vergelijkings functie.</span><span class="sxs-lookup"><span data-stu-id="a161f-105">Given an array, returns whether that array is sorted as defined by a given comparison function.</span></span>

```qsharp
function IsSorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="a161f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a161f-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="a161f-107">vergelijking: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a161f-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a161f-108">Een functie die twee elementen vergelijkt, zodat deze `a` kleiner is dan of gelijk is aan `b` if `comparison(a, b)` `true` .</span><span class="sxs-lookup"><span data-stu-id="a161f-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="a161f-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="a161f-109">array : 'T[]</span></span>

<span data-ttu-id="a161f-110">De matrix die moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="a161f-110">The array to be checked.</span></span>



## <a name="output--bool"></a><span data-ttu-id="a161f-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="a161f-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="a161f-112">`true` Als en alleen als voor elk paar elementen `a` en voor `b` `array` komen in die volg orde, `comparison(a, b)` is `true` .</span><span class="sxs-lookup"><span data-stu-id="a161f-112">`true` if and only if for each pair of elements `a` and `b` of `array` occuring in that order, `comparison(a, b)` is `true`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a161f-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a161f-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a161f-114">T</span><span class="sxs-lookup"><span data-stu-id="a161f-114">'T</span></span>

<span data-ttu-id="a161f-115">Het type van elk element van `array` .</span><span class="sxs-lookup"><span data-stu-id="a161f-115">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a161f-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="a161f-116">Remarks</span></span>

<span data-ttu-id="a161f-117">Er `comparison` wordt van uitgegaan dat de functie transitief is, bijvoorbeeld als `comparison(a, b)` en `comparison(b, c)` `comparison(a, c)` wordt aangenomen.</span><span class="sxs-lookup"><span data-stu-id="a161f-117">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="a161f-118">Als deze eigenschap niet in de wachtrij staat, is de uitvoer van deze functie mogelijk onjuist.</span><span class="sxs-lookup"><span data-stu-id="a161f-118">If this property does not hold, then the output of this function may be incorrect.</span></span>