---
uid: Microsoft.Quantum.Arrays.Interleaved
title: Interleaved functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Interleaved
qsharp.summary: Interleaves two arrays of (almost) same size.
ms.openlocfilehash: 3605c0d0bc43cdb1097d025861c3ec2424763c86
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848120"
---
# <a name="interleaved-function"></a><span data-ttu-id="a08c6-102">Interleaved functie</span><span class="sxs-lookup"><span data-stu-id="a08c6-102">Interleaved function</span></span>

<span data-ttu-id="a08c6-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a08c6-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a08c6-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a08c6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a08c6-105">Interleaving heeft twee matrices van (bijna) dezelfde grootte.</span><span class="sxs-lookup"><span data-stu-id="a08c6-105">Interleaves two arrays of (almost) same size.</span></span>

```qsharp
function Interleaved<'T> (first : 'T[], second : 'T[]) : 'T[]
```


## <a name="description"></a><span data-ttu-id="a08c6-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a08c6-106">Description</span></span>

<span data-ttu-id="a08c6-107">Deze functie retourneert de interleaving van twee matrices, te beginnen met het eerste element van de eerste matrix, vervolgens het eerste element van de tweede matrix, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="a08c6-107">This function returns the interleaving of two arrays, starting with the first element from the first array, then the first element from the second array, and so on.</span></span>

<span data-ttu-id="a08c6-108">De eerste matrix moet even lang zijn als de tweede, of kan een groter element hebben.</span><span class="sxs-lookup"><span data-stu-id="a08c6-108">The first array must either be of the same length as the second one, or can have one more element.</span></span>

## <a name="input"></a><span data-ttu-id="a08c6-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="a08c6-109">Input</span></span>

### <a name="first--t"></a><span data-ttu-id="a08c6-110">First: ' []</span><span class="sxs-lookup"><span data-stu-id="a08c6-110">first : 'T[]</span></span>

<span data-ttu-id="a08c6-111">De eerste matrix die u wilt laten Interleaved.</span><span class="sxs-lookup"><span data-stu-id="a08c6-111">The first array to be interleaved.</span></span>


### <a name="second--t"></a><span data-ttu-id="a08c6-112">seconde: ' []</span><span class="sxs-lookup"><span data-stu-id="a08c6-112">second : 'T[]</span></span>

<span data-ttu-id="a08c6-113">De tweede matrix die u wilt laten Interleaved.</span><span class="sxs-lookup"><span data-stu-id="a08c6-113">The second array to be interleaved.</span></span>



## <a name="output--t"></a><span data-ttu-id="a08c6-114">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="a08c6-114">Output : 'T[]</span></span>

<span data-ttu-id="a08c6-115">Interleaved matrix</span><span class="sxs-lookup"><span data-stu-id="a08c6-115">Interleaved array</span></span>

## <a name="type-parameters"></a><span data-ttu-id="a08c6-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a08c6-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a08c6-117">T</span><span class="sxs-lookup"><span data-stu-id="a08c6-117">'T</span></span>

<span data-ttu-id="a08c6-118">Het type van elk element van `first` en `second` .</span><span class="sxs-lookup"><span data-stu-id="a08c6-118">The type of each element of `first` and `second`.</span></span>

## <a name="example"></a><span data-ttu-id="a08c6-119">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="a08c6-119">Example</span></span>

```qsharp
// same as int1 = [1, -1, 2, -2, 3, -3]
let int1 = Interleaved([1, 2, 3], [-1, -2, -3])

// same as int2 = [false, true, false, true, false]
let int2 = Interleaved(ConstantArray(3, false), ConstantArray(2, true));
```