---
uid: Microsoft.Quantum.Arrays.Swapped
title: Verwissel bare functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Swapped
qsharp.summary: Applies a swap of two elements in an array.
ms.openlocfilehash: fa5b37b4caf5d8f19ed05075ddd7bc4217036bfb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705748"
---
# <a name="swapped-function"></a><span data-ttu-id="aab4b-102">Verwissel bare functie</span><span class="sxs-lookup"><span data-stu-id="aab4b-102">Swapped function</span></span>

<span data-ttu-id="aab4b-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="aab4b-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="aab4b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="aab4b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="aab4b-105">Past een swap van twee elementen in een matrix toe.</span><span class="sxs-lookup"><span data-stu-id="aab4b-105">Applies a swap of two elements in an array.</span></span>

```qsharp
function Swapped<'T> (firstIndex : Int, secondIndex : Int, arr : 'T[]) : 'T[]
```


## <a name="input"></a><span data-ttu-id="aab4b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="aab4b-106">Input</span></span>

### <a name="firstindex--int"></a><span data-ttu-id="aab4b-107">firstIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="aab4b-107">firstIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="aab4b-108">Index van het eerste element dat moet worden omgewisseld.</span><span class="sxs-lookup"><span data-stu-id="aab4b-108">Index of the first element to be swapped.</span></span>


### <a name="secondindex--int"></a><span data-ttu-id="aab4b-109">secondIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="aab4b-109">secondIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="aab4b-110">Index van het tweede element dat moet worden omgewisseld.</span><span class="sxs-lookup"><span data-stu-id="aab4b-110">Index of the second element to be swapped.</span></span>


### <a name="arr--t"></a><span data-ttu-id="aab4b-111">ARR: 'T []</span><span class="sxs-lookup"><span data-stu-id="aab4b-111">arr : 'T[]</span></span>

<span data-ttu-id="aab4b-112">Matrix met elementen die moeten worden omgewisseld.</span><span class="sxs-lookup"><span data-stu-id="aab4b-112">Array with elements to be swapped.</span></span>



## <a name="output--t"></a><span data-ttu-id="aab4b-113">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="aab4b-113">Output : 'T[]</span></span>

<span data-ttu-id="aab4b-114">De matrix met de in-place wisseling toegepast.</span><span class="sxs-lookup"><span data-stu-id="aab4b-114">The array with the in place swap applied.</span></span>

## <a name="example"></a><span data-ttu-id="aab4b-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="aab4b-115">Example</span></span>

```qsharp
// The following returns [0, 3, 2, 1, 4]
Swapped(1, 3, [0, 1, 2, 3, 4]);
```

## <a name="type-parameters"></a><span data-ttu-id="aab4b-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="aab4b-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="aab4b-117">T</span><span class="sxs-lookup"><span data-stu-id="aab4b-117">'T</span></span>
