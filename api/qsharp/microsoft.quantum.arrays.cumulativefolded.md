---
uid: Microsoft.Quantum.Arrays.CumulativeFolded
title: De functie CumulativeFolded
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: CumulativeFolded
qsharp.summary: Combines Mapped and Fold into a single function
ms.openlocfilehash: a09c2779c8f06d8f6b7b0902366f3cefbbca4525
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706125"
---
# <a name="cumulativefolded-function"></a><span data-ttu-id="6f68e-102">De functie CumulativeFolded</span><span class="sxs-lookup"><span data-stu-id="6f68e-102">CumulativeFolded function</span></span>

<span data-ttu-id="6f68e-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="6f68e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="6f68e-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6f68e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6f68e-105">Combineert toegewezen en vouwen in één functie</span><span class="sxs-lookup"><span data-stu-id="6f68e-105">Combines Mapped and Fold into a single function</span></span>

```qsharp
function CumulativeFolded<'State, 'T> (fn : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State[]
```


## <a name="description"></a><span data-ttu-id="6f68e-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6f68e-106">Description</span></span>

<span data-ttu-id="6f68e-107">Met deze functie wordt de `fn` functie herhaald via de matrix, beginnend bij een begin status `state` en worden alle tussenliggende waarden geretourneerd, met inbegrip van de begin status.</span><span class="sxs-lookup"><span data-stu-id="6f68e-107">This function iterates the `fn` function through the array, starting from an initial state `state` and returns all intermediate values, not including the inital state.</span></span>

## <a name="input"></a><span data-ttu-id="6f68e-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="6f68e-108">Input</span></span>

### <a name="fn--statet---state"></a><span data-ttu-id="6f68e-109">FN: (' State, 'T)-> '</span><span class="sxs-lookup"><span data-stu-id="6f68e-109">fn : ('State,'T) -> 'State</span></span>

<span data-ttu-id="6f68e-110">Een functie die in de matrix moet worden gevouwen</span><span class="sxs-lookup"><span data-stu-id="6f68e-110">A function to be folded over the array</span></span>


### <a name="state--state"></a><span data-ttu-id="6f68e-111">status: ' State</span><span class="sxs-lookup"><span data-stu-id="6f68e-111">state : 'State</span></span>

<span data-ttu-id="6f68e-112">De begin status die moet worden gevouwen</span><span class="sxs-lookup"><span data-stu-id="6f68e-112">The initial state to be folded</span></span>


### <a name="array--t"></a><span data-ttu-id="6f68e-113">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="6f68e-113">array : 'T[]</span></span>

<span data-ttu-id="6f68e-114">Een matrix met waarden die moeten worden gevouwen</span><span class="sxs-lookup"><span data-stu-id="6f68e-114">An array of values to be folded over</span></span>



## <a name="output--state"></a><span data-ttu-id="6f68e-115">Uitvoer: ' status []</span><span class="sxs-lookup"><span data-stu-id="6f68e-115">Output : 'State[]</span></span>

<span data-ttu-id="6f68e-116">Alle tussenliggende statussen, inclusief de eind status, maar niet de begin status.</span><span class="sxs-lookup"><span data-stu-id="6f68e-116">All intermediate states, including the final state, but not the initial state.</span></span>
<span data-ttu-id="6f68e-117">De lengte van de uitvoer matrix heeft dezelfde lengte als `array` .</span><span class="sxs-lookup"><span data-stu-id="6f68e-117">The length of the output array is of the same length as `array`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="6f68e-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="6f68e-118">Type Parameters</span></span>

### <a name="state"></a><span data-ttu-id="6f68e-119">' Status</span><span class="sxs-lookup"><span data-stu-id="6f68e-119">'State</span></span>

<span data-ttu-id="6f68e-120">Het type statussen waarop de `fn` functie wordt uitgevoerd, dat wil zeggen, accepteert als eerste invoer en retourneert.</span><span class="sxs-lookup"><span data-stu-id="6f68e-120">The type of states that the `fn` function operates on, i.e., accepts as its first input and returns.</span></span>
### <a name="t"></a><span data-ttu-id="6f68e-121">T</span><span class="sxs-lookup"><span data-stu-id="6f68e-121">'T</span></span>

<span data-ttu-id="6f68e-122">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="6f68e-122">The type of `array` elements.</span></span>