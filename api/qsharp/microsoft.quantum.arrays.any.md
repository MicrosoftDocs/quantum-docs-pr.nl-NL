---
uid: Microsoft.Quantum.Arrays.Any
title: Een functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Any
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.
ms.openlocfilehash: a05f9531168bf2b32977665d38cc00f3c8e64879
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846270"
---
# <a name="any-function"></a><span data-ttu-id="fb106-102">Een functie</span><span class="sxs-lookup"><span data-stu-id="fb106-102">Any function</span></span>

<span data-ttu-id="fb106-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="fb106-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="fb106-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fb106-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fb106-105">Op basis van een matrix en een predikaat die is gedefinieerd voor de elementen van de matrix, wordt gecontroleerd of ten minste één element van de matrix voldoet aan het predicaat.</span><span class="sxs-lookup"><span data-stu-id="fb106-105">Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.</span></span>

```qsharp
function Any<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="fb106-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="fb106-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="fb106-107">predikaat: niet-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="fb106-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="fb106-108">Een functie van `'T` naar `Bool` die wordt gebruikt om elementen te controleren.</span><span class="sxs-lookup"><span data-stu-id="fb106-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="fb106-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="fb106-109">array : 'T[]</span></span>

<span data-ttu-id="fb106-110">Een matrix van elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="fb106-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="fb106-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="fb106-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="fb106-112">Een `Bool` waarde van de functie or van het predikaat dat is toegepast op alle elementen.</span><span class="sxs-lookup"><span data-stu-id="fb106-112">A `Bool` value of the OR function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="fb106-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="fb106-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="fb106-114">T</span><span class="sxs-lookup"><span data-stu-id="fb106-114">'T</span></span>

<span data-ttu-id="fb106-115">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="fb106-115">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="fb106-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="fb106-116">Example</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function IsThreePresent() : Bool {
    let arrayOfInts = [1, 2, 3, 4, 5];
    let is3Present = IsNumberPresentInArray(3, arrayOfInts);
    return is3Present;
}

function IsNumberPresentInArray(n : Int, array : Int[]) : Bool {
    return Any(EqualI(_, n), array);
}
```

## <a name="remarks"></a><span data-ttu-id="fb106-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="fb106-117">Remarks</span></span>

<span data-ttu-id="fb106-118">De functie is gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix `'T[]` en een functie hebben `predicate: 'T -> Bool` die we een `Bool` waarde kunnen produceren die aangeeft of een bepaald element voldoet aan het resultaat `predicate` .</span><span class="sxs-lookup"><span data-stu-id="fb106-118">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if some element satisfies `predicate`.</span></span>