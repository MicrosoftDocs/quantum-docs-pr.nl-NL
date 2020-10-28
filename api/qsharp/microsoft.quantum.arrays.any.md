---
uid: Microsoft.Quantum.Arrays.Any
title: Een functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Any
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.
ms.openlocfilehash: dd5639f1b0a76cb356c89aca0c0e02d375f30d12
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706180"
---
# <a name="any-function"></a><span data-ttu-id="4631b-102">Een functie</span><span class="sxs-lookup"><span data-stu-id="4631b-102">Any function</span></span>

<span data-ttu-id="4631b-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="4631b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="4631b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="4631b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="4631b-105">Op basis van een matrix en een predikaat die is gedefinieerd voor de elementen van de matrix, wordt gecontroleerd of ten minste één element van de matrix voldoet aan het predicaat.</span><span class="sxs-lookup"><span data-stu-id="4631b-105">Given an array and a predicate that is defined for the elements of the array, checks if at least one element of the array satisfies the predicate.</span></span>

```qsharp
function Any<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="4631b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="4631b-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="4631b-107">predikaat: niet-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4631b-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4631b-108">Een functie van `'T` naar `Bool` die wordt gebruikt om elementen te controleren.</span><span class="sxs-lookup"><span data-stu-id="4631b-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="4631b-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="4631b-109">array : 'T[]</span></span>

<span data-ttu-id="4631b-110">Een matrix van elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="4631b-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="4631b-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="4631b-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="4631b-112">Een `Bool` waarde van de functie or van het predikaat dat is toegepast op alle elementen.</span><span class="sxs-lookup"><span data-stu-id="4631b-112">A `Bool` value of the OR function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="4631b-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="4631b-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="4631b-114">T</span><span class="sxs-lookup"><span data-stu-id="4631b-114">'T</span></span>

<span data-ttu-id="4631b-115">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="4631b-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="4631b-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="4631b-116">Remarks</span></span>

<span data-ttu-id="4631b-117">De functie is gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix `'T[]` en een functie hebben `predicate: 'T -> Bool` die we een `Bool` waarde kunnen produceren die aangeeft of een bepaald element voldoet aan het resultaat `predicate` .</span><span class="sxs-lookup"><span data-stu-id="4631b-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if some element satisfies `predicate`.</span></span>