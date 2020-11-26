---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Interleaved functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 1ff5999cc19f47e3dcae601b960446923b613d90
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220957"
---
# <a name="interleaved-function"></a><span data-ttu-id="e030c-102">Interleaved functie</span><span class="sxs-lookup"><span data-stu-id="e030c-102">Interleaved function</span></span>

<span data-ttu-id="e030c-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="e030c-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="e030c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e030c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e030c-105">Interleaving heeft twee matrices van (bijna) dezelfde grootte.</span><span class="sxs-lookup"><span data-stu-id="e030c-105">Interleaves two arrays of (almost) same size.</span></span>

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="e030c-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e030c-106">Description</span></span>

<span data-ttu-id="e030c-107">Deze functie retourneert de interleaving van twee matrices, te beginnen met het eerste element van de eerste matrix, vervolgens het eerste element van de tweede matrix, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="e030c-107">This function returns the interleaving of two arrays, starting with the first element from the first array, then the first element from the second array, and so on.</span></span>

<span data-ttu-id="e030c-108">De eerste matrix moet even lang zijn als de tweede, of kan een groter element hebben.</span><span class="sxs-lookup"><span data-stu-id="e030c-108">The first array must either be of the same length as the second one, or can have one more element.</span></span>

## <a name="input"></a><span data-ttu-id="e030c-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="e030c-109">Input</span></span>

### <a name="first--t"></a><span data-ttu-id="e030c-110">First: ' []</span><span class="sxs-lookup"><span data-stu-id="e030c-110">first : 'T[]</span></span>

<span data-ttu-id="e030c-111">De eerste matrix die u wilt laten Interleaved.</span><span class="sxs-lookup"><span data-stu-id="e030c-111">The first array to be interleaved.</span></span>


### <a name="second--t"></a><span data-ttu-id="e030c-112">seconde: ' []</span><span class="sxs-lookup"><span data-stu-id="e030c-112">second : 'T[]</span></span>

<span data-ttu-id="e030c-113">De tweede matrix die u wilt laten Interleaved.</span><span class="sxs-lookup"><span data-stu-id="e030c-113">The second array to be interleaved.</span></span>



## <a name="output--t"></a><span data-ttu-id="e030c-114">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="e030c-114">Output : 'T[]</span></span>

<span data-ttu-id="e030c-115">Interleaved matrix</span><span class="sxs-lookup"><span data-stu-id="e030c-115">Interleaved array</span></span>

## <a name="type-parameters"></a><span data-ttu-id="e030c-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e030c-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e030c-117">T</span><span class="sxs-lookup"><span data-stu-id="e030c-117">'T</span></span>

<span data-ttu-id="e030c-118">Het type van elk element van `first` en `second` .</span><span class="sxs-lookup"><span data-stu-id="e030c-118">The type of each element of `first` and `second`.</span></span>