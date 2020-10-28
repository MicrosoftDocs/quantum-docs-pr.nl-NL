---
uid: Microsoft.Quantum.Arrays.Fold
title: Functie vouwen
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: 47c23dd657391d80fe473d98f2036d8ddf1dbb0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706004"
---
# <a name="fold-function"></a><span data-ttu-id="b01ba-102">Functie vouwen</span><span class="sxs-lookup"><span data-stu-id="b01ba-102">Fold function</span></span>

<span data-ttu-id="b01ba-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="b01ba-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="b01ba-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="b01ba-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="b01ba-105">Herhaalt een functie `f` via een matrix `array` , waarbij wordt geretourneerd `f(f(f(initialState, array[0]), array[1]), ...)` .</span><span class="sxs-lookup"><span data-stu-id="b01ba-105">Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.</span></span>

```qsharp
function Fold<'State, 'T> (folder : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State
```


## <a name="input"></a><span data-ttu-id="b01ba-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b01ba-106">Input</span></span>

### <a name="folder--statet---state"></a><span data-ttu-id="b01ba-107">map: (status, niet)-> status</span><span class="sxs-lookup"><span data-stu-id="b01ba-107">folder : ('State,'T) -> 'State</span></span>

<span data-ttu-id="b01ba-108">Een functie die over de matrix moet worden gevouwen.</span><span class="sxs-lookup"><span data-stu-id="b01ba-108">A function to be folded over the array.</span></span>


### <a name="state--state"></a><span data-ttu-id="b01ba-109">status: ' State</span><span class="sxs-lookup"><span data-stu-id="b01ba-109">state : 'State</span></span>

<span data-ttu-id="b01ba-110">De oorspronkelijke status van de map.</span><span class="sxs-lookup"><span data-stu-id="b01ba-110">The initial state of the folder.</span></span>


### <a name="array--t"></a><span data-ttu-id="b01ba-111">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="b01ba-111">array : 'T[]</span></span>

<span data-ttu-id="b01ba-112">Een matrix met waarden die moeten worden gevouwen.</span><span class="sxs-lookup"><span data-stu-id="b01ba-112">An array of values to be folded over.</span></span>



## <a name="output--state"></a><span data-ttu-id="b01ba-113">Uitvoer: ' State</span><span class="sxs-lookup"><span data-stu-id="b01ba-113">Output : 'State</span></span>

<span data-ttu-id="b01ba-114">De uiteindelijke status die is geretourneerd door de map na het herhalen van alle elementen van `array` .</span><span class="sxs-lookup"><span data-stu-id="b01ba-114">The final state returned by the folder after iterating over all elements of `array`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="b01ba-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="b01ba-115">Type Parameters</span></span>

### <a name="state"></a><span data-ttu-id="b01ba-116">' Status</span><span class="sxs-lookup"><span data-stu-id="b01ba-116">'State</span></span>

<span data-ttu-id="b01ba-117">Het type statussen waarop de functie wordt uitgevoerd `folder` , dat wil zeggen, accepteert als eerste argument en retourneert.</span><span class="sxs-lookup"><span data-stu-id="b01ba-117">The type of states the `folder` function operates on, i.e., accepts as its first argument and returns.</span></span>
### <a name="t"></a><span data-ttu-id="b01ba-118">T</span><span class="sxs-lookup"><span data-stu-id="b01ba-118">'T</span></span>

<span data-ttu-id="b01ba-119">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="b01ba-119">The type of `array` elements.</span></span>