---
uid: Microsoft.Quantum.Arrays.All
title: Functie all
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: All
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.
ms.openlocfilehash: 345c3fb92babd4ae2e54803b6c3b79b3313ef417
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706181"
---
# <a name="all-function"></a><span data-ttu-id="717f9-102">Functie all</span><span class="sxs-lookup"><span data-stu-id="717f9-102">All function</span></span>

<span data-ttu-id="717f9-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="717f9-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="717f9-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="717f9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="717f9-105">Gegeven een matrix en een predikaat die is gedefinieerd voor de elementen van de matrix en controleert of alle elementen van de matrix voldoen aan het predicaat.</span><span class="sxs-lookup"><span data-stu-id="717f9-105">Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.</span></span>

```qsharp
function All<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="717f9-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="717f9-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="717f9-107">predikaat: niet-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="717f9-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="717f9-108">Een functie van `'T` naar `Bool` die wordt gebruikt om elementen te controleren.</span><span class="sxs-lookup"><span data-stu-id="717f9-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="717f9-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="717f9-109">array : 'T[]</span></span>

<span data-ttu-id="717f9-110">Een matrix van elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="717f9-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="717f9-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="717f9-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="717f9-112">Een `Bool` waarde van de functie en van het predikaat dat is toegepast op alle elementen.</span><span class="sxs-lookup"><span data-stu-id="717f9-112">A `Bool` value of the AND function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="717f9-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="717f9-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="717f9-114">T</span><span class="sxs-lookup"><span data-stu-id="717f9-114">'T</span></span>

<span data-ttu-id="717f9-115">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="717f9-115">The type of `array` elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="717f9-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="717f9-116">Remarks</span></span>

<span data-ttu-id="717f9-117">De functie is gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix `'T[]` en een functie hebben `predicate: 'T -> Bool` die we een `Bool` waarde kunnen produceren die aangeeft of alle elementen voldoen `predicate` .</span><span class="sxs-lookup"><span data-stu-id="717f9-117">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if all elements satisfy `predicate`.</span></span>