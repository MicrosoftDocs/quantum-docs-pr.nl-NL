---
uid: Microsoft.Quantum.Arrays.IsSorted
title: De functie IsSorted
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsSorted
qsharp.summary: Given an array, returns whether that array is sorted as defined by a given comparison function.
ms.openlocfilehash: b2c5f11c0d92ddf9214de2d439c175319c569be0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220828"
---
# <a name="issorted-function"></a><span data-ttu-id="60b97-102">De functie IsSorted</span><span class="sxs-lookup"><span data-stu-id="60b97-102">IsSorted function</span></span>

<span data-ttu-id="60b97-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="60b97-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="60b97-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="60b97-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="60b97-105">Retourneert aan de hand van een matrix of die matrix is gesorteerd zoals gedefinieerd door een bepaalde vergelijkings functie.</span><span class="sxs-lookup"><span data-stu-id="60b97-105">Given an array, returns whether that array is sorted as defined by a given comparison function.</span></span>

```qsharp
function IsSorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="60b97-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="60b97-106">Input</span></span>

### <a name="comparison--tt---bool"></a><span data-ttu-id="60b97-107">vergelijking: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="60b97-107">comparison : ('T,'T) -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="60b97-108">Een functie die twee elementen vergelijkt, zodat deze `a` kleiner is dan of gelijk is aan `b` if `comparison(a, b)` `true` .</span><span class="sxs-lookup"><span data-stu-id="60b97-108">A function that compares two elements such that `a` is considered to be less than or equal to `b` if `comparison(a, b)` is `true`.</span></span>


### <a name="array--t"></a><span data-ttu-id="60b97-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="60b97-109">array : 'T[]</span></span>

<span data-ttu-id="60b97-110">De matrix die moet worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="60b97-110">The array to be checked.</span></span>



## <a name="output--bool"></a><span data-ttu-id="60b97-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="60b97-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="60b97-112">`true` Als en alleen als voor elk paar elementen `a` en voor `b` `array` komen in die volg orde, `comparison(a, b)` is `true` .</span><span class="sxs-lookup"><span data-stu-id="60b97-112">`true` if and only if for each pair of elements `a` and `b` of `array` occuring in that order, `comparison(a, b)` is `true`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="60b97-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="60b97-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="60b97-114">T</span><span class="sxs-lookup"><span data-stu-id="60b97-114">'T</span></span>

<span data-ttu-id="60b97-115">Het type van elk element van `array` .</span><span class="sxs-lookup"><span data-stu-id="60b97-115">The type of each element of `array`.</span></span>

## <a name="remarks"></a><span data-ttu-id="60b97-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="60b97-116">Remarks</span></span>

<span data-ttu-id="60b97-117">Er `comparison` wordt van uitgegaan dat de functie transitief is, bijvoorbeeld als `comparison(a, b)` en `comparison(b, c)` `comparison(a, c)` wordt aangenomen.</span><span class="sxs-lookup"><span data-stu-id="60b97-117">The function `comparison` is assumed to be transitive, such that if `comparison(a, b)` and `comparison(b, c)`, then `comparison(a, c)` is assumed.</span></span> <span data-ttu-id="60b97-118">Als deze eigenschap niet in de wachtrij staat, is de uitvoer van deze functie mogelijk onjuist.</span><span class="sxs-lookup"><span data-stu-id="60b97-118">If this property does not hold, then the output of this function may be incorrect.</span></span>