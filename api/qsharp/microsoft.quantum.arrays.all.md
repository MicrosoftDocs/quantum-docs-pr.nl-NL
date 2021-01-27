---
uid: Microsoft.Quantum.Arrays.All
title: Functie all
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: All
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.
ms.openlocfilehash: 17e61ea161b90fe089b7df7c10188d604d72dcfa
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842901"
---
# <a name="all-function"></a><span data-ttu-id="7c183-102">Functie all</span><span class="sxs-lookup"><span data-stu-id="7c183-102">All function</span></span>

<span data-ttu-id="7c183-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7c183-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7c183-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7c183-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7c183-105">Gegeven een matrix en een predikaat die is gedefinieerd voor de elementen van de matrix en controleert of alle elementen van de matrix voldoen aan het predicaat.</span><span class="sxs-lookup"><span data-stu-id="7c183-105">Given an array and a predicate that is defined for the elements of the array, and checks if all elements of the array satisfy the predicate.</span></span>

```qsharp
function All<'T> (predicate : ('T -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a><span data-ttu-id="7c183-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="7c183-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="7c183-107">predikaat: niet-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="7c183-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7c183-108">Een functie van `'T` naar `Bool` die wordt gebruikt om elementen te controleren.</span><span class="sxs-lookup"><span data-stu-id="7c183-108">A function from `'T` to `Bool` that is used to check elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="7c183-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="7c183-109">array : 'T[]</span></span>

<span data-ttu-id="7c183-110">Een matrix van elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="7c183-110">An array of elements over `'T`.</span></span>



## <a name="output--bool"></a><span data-ttu-id="7c183-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="7c183-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="7c183-112">Een `Bool` waarde van de functie en van het predikaat dat is toegepast op alle elementen.</span><span class="sxs-lookup"><span data-stu-id="7c183-112">A `Bool` value of the AND function of the predicate applied to all elements.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7c183-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="7c183-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="7c183-114">T</span><span class="sxs-lookup"><span data-stu-id="7c183-114">'T</span></span>

<span data-ttu-id="7c183-115">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="7c183-115">The type of `array` elements.</span></span>

## <a name="example"></a><span data-ttu-id="7c183-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="7c183-116">Example</span></span>

<span data-ttu-id="7c183-117">Met de volgende code wordt gecontroleerd of alle elementen van de matrix niet-nul zijn:</span><span class="sxs-lookup"><span data-stu-id="7c183-117">The following code checks whether all elements of the array are non-zero:</span></span>

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function AllDemo() : Unit {
    let predicate = NotEqualI(_, 0);
    let isNonZero = All(predicate, [2, 3, 4, 5, 6, 0]);
    Message($"{isNonZero}");
}
```

## <a name="remarks"></a><span data-ttu-id="7c183-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="7c183-118">Remarks</span></span>

<span data-ttu-id="7c183-119">De functie is gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix `'T[]` en een functie hebben `predicate: 'T -> Bool` die we een `Bool` waarde kunnen produceren die aangeeft of alle elementen voldoen `predicate` .</span><span class="sxs-lookup"><span data-stu-id="7c183-119">The function is defined for generic types, i.e., whenever we have an array `'T[]` and a function `predicate: 'T -> Bool` we can produce a `Bool` value that indicates if all elements satisfy `predicate`.</span></span>