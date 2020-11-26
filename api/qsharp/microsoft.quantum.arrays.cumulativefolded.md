---
uid: Microsoft.Quantum.Arrays.CumulativeFolded
title: De functie CumulativeFolded
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: CumulativeFolded
qsharp.summary: Combines Mapped and Fold into a single function
ms.openlocfilehash: ffb934d06f6be06cbc35a523c90d2c54e0a51353
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210026"
---
# <a name="cumulativefolded-function"></a><span data-ttu-id="19d04-102">De functie CumulativeFolded</span><span class="sxs-lookup"><span data-stu-id="19d04-102">CumulativeFolded function</span></span>

<span data-ttu-id="19d04-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="19d04-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="19d04-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="19d04-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="19d04-105">Combineert toegewezen en vouwen in één functie</span><span class="sxs-lookup"><span data-stu-id="19d04-105">Combines Mapped and Fold into a single function</span></span>

```qsharp
function CumulativeFolded<'State, 'T> (fn : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State[]
```


## <a name="description"></a><span data-ttu-id="19d04-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="19d04-106">Description</span></span>

<span data-ttu-id="19d04-107">Met deze functie wordt de `fn` functie herhaald via de matrix, beginnend bij een begin status `state` en worden alle tussenliggende waarden geretourneerd, met inbegrip van de begin status.</span><span class="sxs-lookup"><span data-stu-id="19d04-107">This function iterates the `fn` function through the array, starting from an initial state `state` and returns all intermediate values, not including the inital state.</span></span>

## <a name="input"></a><span data-ttu-id="19d04-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="19d04-108">Input</span></span>

### <a name="fn--statet---state"></a><span data-ttu-id="19d04-109">FN: (' State, 'T)-> '</span><span class="sxs-lookup"><span data-stu-id="19d04-109">fn : ('State,'T) -> 'State</span></span>

<span data-ttu-id="19d04-110">Een functie die in de matrix moet worden gevouwen</span><span class="sxs-lookup"><span data-stu-id="19d04-110">A function to be folded over the array</span></span>


### <a name="state--state"></a><span data-ttu-id="19d04-111">status: ' State</span><span class="sxs-lookup"><span data-stu-id="19d04-111">state : 'State</span></span>

<span data-ttu-id="19d04-112">De begin status die moet worden gevouwen</span><span class="sxs-lookup"><span data-stu-id="19d04-112">The initial state to be folded</span></span>


### <a name="array--t"></a><span data-ttu-id="19d04-113">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="19d04-113">array : 'T[]</span></span>

<span data-ttu-id="19d04-114">Een matrix met waarden die moeten worden gevouwen</span><span class="sxs-lookup"><span data-stu-id="19d04-114">An array of values to be folded over</span></span>



## <a name="output--state"></a><span data-ttu-id="19d04-115">Uitvoer: ' status []</span><span class="sxs-lookup"><span data-stu-id="19d04-115">Output : 'State[]</span></span>

<span data-ttu-id="19d04-116">Alle tussenliggende statussen, inclusief de eind status, maar niet de begin status.</span><span class="sxs-lookup"><span data-stu-id="19d04-116">All intermediate states, including the final state, but not the initial state.</span></span>
<span data-ttu-id="19d04-117">De lengte van de uitvoer matrix heeft dezelfde lengte als `array` .</span><span class="sxs-lookup"><span data-stu-id="19d04-117">The length of the output array is of the same length as `array`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="19d04-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="19d04-118">Type Parameters</span></span>

### <a name="state"></a><span data-ttu-id="19d04-119">' Status</span><span class="sxs-lookup"><span data-stu-id="19d04-119">'State</span></span>

<span data-ttu-id="19d04-120">Het type statussen waarop de `fn` functie wordt uitgevoerd, dat wil zeggen, accepteert als eerste invoer en retourneert.</span><span class="sxs-lookup"><span data-stu-id="19d04-120">The type of states that the `fn` function operates on, i.e., accepts as its first input and returns.</span></span>
### <a name="t"></a><span data-ttu-id="19d04-121">T</span><span class="sxs-lookup"><span data-stu-id="19d04-121">'T</span></span>

<span data-ttu-id="19d04-122">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="19d04-122">The type of `array` elements.</span></span>