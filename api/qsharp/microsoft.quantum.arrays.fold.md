---
uid: Microsoft.Quantum.Arrays.Fold
title: Functie vouwen
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: a42f9a832c18bd612c1ae416187f3f2513eed54d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221161"
---
# <a name="fold-function"></a><span data-ttu-id="00e4d-102">Functie vouwen</span><span class="sxs-lookup"><span data-stu-id="00e4d-102">Fold function</span></span>

<span data-ttu-id="00e4d-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="00e4d-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="00e4d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="00e4d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="00e4d-105">Herhaalt een functie `f` via een matrix `array` , waarbij wordt geretourneerd `f(f(f(initialState, array[0]), array[1]), ...)` .</span><span class="sxs-lookup"><span data-stu-id="00e4d-105">Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.</span></span>

```qsharp
function Fold<'State, 'T> (folder : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State
```


## <a name="input"></a><span data-ttu-id="00e4d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="00e4d-106">Input</span></span>

### <a name="folder--statet---state"></a><span data-ttu-id="00e4d-107">map: (status, niet)-> status</span><span class="sxs-lookup"><span data-stu-id="00e4d-107">folder : ('State,'T) -> 'State</span></span>

<span data-ttu-id="00e4d-108">Een functie die over de matrix moet worden gevouwen.</span><span class="sxs-lookup"><span data-stu-id="00e4d-108">A function to be folded over the array.</span></span>


### <a name="state--state"></a><span data-ttu-id="00e4d-109">status: ' State</span><span class="sxs-lookup"><span data-stu-id="00e4d-109">state : 'State</span></span>

<span data-ttu-id="00e4d-110">De oorspronkelijke status van de map.</span><span class="sxs-lookup"><span data-stu-id="00e4d-110">The initial state of the folder.</span></span>


### <a name="array--t"></a><span data-ttu-id="00e4d-111">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="00e4d-111">array : 'T[]</span></span>

<span data-ttu-id="00e4d-112">Een matrix met waarden die moeten worden gevouwen.</span><span class="sxs-lookup"><span data-stu-id="00e4d-112">An array of values to be folded over.</span></span>



## <a name="output--state"></a><span data-ttu-id="00e4d-113">Uitvoer: ' State</span><span class="sxs-lookup"><span data-stu-id="00e4d-113">Output : 'State</span></span>

<span data-ttu-id="00e4d-114">De uiteindelijke status die is geretourneerd door de map na het herhalen van alle elementen van `array` .</span><span class="sxs-lookup"><span data-stu-id="00e4d-114">The final state returned by the folder after iterating over all elements of `array`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="00e4d-115">Type parameters</span><span class="sxs-lookup"><span data-stu-id="00e4d-115">Type Parameters</span></span>

### <a name="state"></a><span data-ttu-id="00e4d-116">' Status</span><span class="sxs-lookup"><span data-stu-id="00e4d-116">'State</span></span>

<span data-ttu-id="00e4d-117">Het type statussen waarop de functie wordt uitgevoerd `folder` , dat wil zeggen, accepteert als eerste argument en retourneert.</span><span class="sxs-lookup"><span data-stu-id="00e4d-117">The type of states the `folder` function operates on, i.e., accepts as its first argument and returns.</span></span>
### <a name="t"></a><span data-ttu-id="00e4d-118">T</span><span class="sxs-lookup"><span data-stu-id="00e4d-118">'T</span></span>

<span data-ttu-id="00e4d-119">Het type `array` elementen.</span><span class="sxs-lookup"><span data-stu-id="00e4d-119">The type of `array` elements.</span></span>