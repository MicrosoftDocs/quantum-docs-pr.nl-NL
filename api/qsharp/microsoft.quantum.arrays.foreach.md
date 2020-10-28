---
uid: Microsoft.Quantum.Arrays.ForEach
title: ForEach-bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: ab6ac6eb913095f31ba166ac27f034f2e2875acf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705997"
---
# <a name="foreach-operation"></a><span data-ttu-id="cbcc8-102">ForEach-bewerking</span><span class="sxs-lookup"><span data-stu-id="cbcc8-102">ForEach operation</span></span>

<span data-ttu-id="cbcc8-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="cbcc8-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="cbcc8-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="cbcc8-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="cbcc8-105">Op basis van een matrix en een bewerking die is gedefinieerd voor de elementen van de matrix, retourneert een nieuwe matrix die bestaat uit de installatie kopieën van de oorspronkelijke matrix onder de bewerking.</span><span class="sxs-lookup"><span data-stu-id="cbcc8-105">Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.</span></span>

```qsharp
operation ForEach<'T, 'U> (action : ('T => 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a><span data-ttu-id="cbcc8-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="cbcc8-106">Input</span></span>

### <a name="action--t--u"></a><span data-ttu-id="cbcc8-107">actie: 'T => ' U</span><span class="sxs-lookup"><span data-stu-id="cbcc8-107">action : 'T => 'U</span></span> 

<span data-ttu-id="cbcc8-108">Een bewerking van `'T` naar `'U` die wordt toegepast op elk element.</span><span class="sxs-lookup"><span data-stu-id="cbcc8-108">An operation from `'T` to `'U` that is applied to each element.</span></span>


### <a name="array--t"></a><span data-ttu-id="cbcc8-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="cbcc8-109">array : 'T[]</span></span>

<span data-ttu-id="cbcc8-110">Een matrix van elementen `'T` .</span><span class="sxs-lookup"><span data-stu-id="cbcc8-110">An array of elements over `'T`.</span></span>



## <a name="output--u"></a><span data-ttu-id="cbcc8-111">Uitvoer: ' U []</span><span class="sxs-lookup"><span data-stu-id="cbcc8-111">Output : 'U[]</span></span>

<span data-ttu-id="cbcc8-112">Een matrix `'U[]` met elementen die worden toegewezen door de `action` bewerking.</span><span class="sxs-lookup"><span data-stu-id="cbcc8-112">An array `'U[]` of elements that are mapped by the `action` operation.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="cbcc8-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="cbcc8-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cbcc8-114">T</span><span class="sxs-lookup"><span data-stu-id="cbcc8-114">'T</span></span>

<span data-ttu-id="cbcc8-115">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="cbcc8-115">The type of `array` elements.</span></span>
### <a name="u"></a><span data-ttu-id="cbcc8-116">' U</span><span class="sxs-lookup"><span data-stu-id="cbcc8-116">'U</span></span>

<span data-ttu-id="cbcc8-117">Het resultaat type van de `action` bewerking.</span><span class="sxs-lookup"><span data-stu-id="cbcc8-117">The result type of the `action` operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbcc8-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="cbcc8-118">Remarks</span></span>

<span data-ttu-id="cbcc8-119">De bewerking wordt gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix `'T[]` en een bewerking hebben `action : 'T -> 'U` die de elementen van de matrix kunnen toewijzen en een nieuwe matrix van het type maken `'U[]` .</span><span class="sxs-lookup"><span data-stu-id="cbcc8-119">The operation is defined for generic types, i.e., whenever we have an array `'T[]` and an operation `action : 'T -> 'U` we can map the elements of the array and produce a new array of type `'U[]`.</span></span>