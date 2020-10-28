---
uid: Microsoft.Quantum.Arrays.Where
title: Functie where
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Where
qsharp.summary: Given a predicate and an array, returns the indices of that array where the predicate is true.
ms.openlocfilehash: 1c9fa0463ed49788d12502257d735b965565d1ab
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705700"
---
# <a name="where-function"></a><span data-ttu-id="81763-102">Functie where</span><span class="sxs-lookup"><span data-stu-id="81763-102">Where function</span></span>

<span data-ttu-id="81763-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="81763-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="81763-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="81763-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="81763-105">Op basis van een predikaat en een matrix, worden de indexen van die matrix geretourneerd waarbij het predicaat True is.</span><span class="sxs-lookup"><span data-stu-id="81763-105">Given a predicate and an array, returns the indices of that array where the predicate is true.</span></span>

```qsharp
function Where<'T> (predicate : ('T -> Bool), array : 'T[]) : Int[]
```


## <a name="input"></a><span data-ttu-id="81763-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="81763-106">Input</span></span>

### <a name="predicate--t---bool"></a><span data-ttu-id="81763-107">predikaat: niet-> [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="81763-107">predicate : 'T -> [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="81763-108">Een functie van `'T` naar een Booleaanse waarde die wordt gebruikt voor het filteren van elementen.</span><span class="sxs-lookup"><span data-stu-id="81763-108">A function from `'T` to Boolean that is used to filter elements.</span></span>


### <a name="array--t"></a><span data-ttu-id="81763-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="81763-109">array : 'T[]</span></span>

<span data-ttu-id="81763-110">Een matrix van elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="81763-110">An array of elements over `'T`.</span></span>



## <a name="output--int"></a><span data-ttu-id="81763-111">Output: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="81763-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="81763-112">Een matrix met indices waar `predicate` is waar.</span><span class="sxs-lookup"><span data-stu-id="81763-112">An array of indices where `predicate` is true.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="81763-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="81763-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="81763-114">T</span><span class="sxs-lookup"><span data-stu-id="81763-114">'T</span></span>

<span data-ttu-id="81763-115">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="81763-115">The type of `array` elements.</span></span>