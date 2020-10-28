---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Interleaved functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 8405cabca17f2dd7c2680833bfab5c3768fcf752
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705957"
---
# <a name="interleaved-function"></a><span data-ttu-id="02a94-102">Interleaved functie</span><span class="sxs-lookup"><span data-stu-id="02a94-102">Interleaved function</span></span>

<span data-ttu-id="02a94-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="02a94-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="02a94-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="02a94-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="02a94-105">Interleaving heeft twee matrices van (bijna) dezelfde grootte.</span><span class="sxs-lookup"><span data-stu-id="02a94-105">Interleaves two arrays of (almost) same size.</span></span>

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="02a94-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="02a94-106">Description</span></span>

<span data-ttu-id="02a94-107">Deze functie retourneert de interleaving van twee matrices, te beginnen met het eerste element van de eerste matrix, vervolgens het eerste element van de tweede matrix, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="02a94-107">This function returns the interleaving of two arrays, starting with the first element from the first array, then the first element from the second array, and so on.</span></span>

<span data-ttu-id="02a94-108">De eerste matrix moet even lang zijn als de tweede, of kan een groter element hebben.</span><span class="sxs-lookup"><span data-stu-id="02a94-108">The first array must either be of the same length as the second one, or can have one more element.</span></span>

## <a name="input"></a><span data-ttu-id="02a94-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="02a94-109">Input</span></span>

### <a name="first--t"></a><span data-ttu-id="02a94-110">First: ' []</span><span class="sxs-lookup"><span data-stu-id="02a94-110">first : 'T[]</span></span>

<span data-ttu-id="02a94-111">De eerste matrix die u wilt laten Interleaved.</span><span class="sxs-lookup"><span data-stu-id="02a94-111">The first array to be interleaved.</span></span>


### <a name="second--t"></a><span data-ttu-id="02a94-112">seconde: ' []</span><span class="sxs-lookup"><span data-stu-id="02a94-112">second : 'T[]</span></span>

<span data-ttu-id="02a94-113">De tweede matrix die u wilt laten Interleaved.</span><span class="sxs-lookup"><span data-stu-id="02a94-113">The second array to be interleaved.</span></span>



## <a name="output--t"></a><span data-ttu-id="02a94-114">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="02a94-114">Output : 'T[]</span></span>

<span data-ttu-id="02a94-115">Interleaved matrix</span><span class="sxs-lookup"><span data-stu-id="02a94-115">Interleaved array</span></span>

## <a name="type-parameters"></a><span data-ttu-id="02a94-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="02a94-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="02a94-117">T</span><span class="sxs-lookup"><span data-stu-id="02a94-117">'T</span></span>

<span data-ttu-id="02a94-118">Het type van elk element van `first` en `second` .</span><span class="sxs-lookup"><span data-stu-id="02a94-118">The type of each element of `first` and `second`.</span></span>