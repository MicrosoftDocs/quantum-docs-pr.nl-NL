---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Uitgepakte functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: 7eea7982721dc596b8660be5f3634df71b1ddf95
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845369"
---
# <a name="unzipped-function"></a><span data-ttu-id="df705-102">Uitgepakte functie</span><span class="sxs-lookup"><span data-stu-id="df705-102">Unzipped function</span></span>

<span data-ttu-id="df705-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="df705-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="df705-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="df705-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="df705-105">Op basis van een matrix van 2-Tuples retourneert een tuple van twee matrices, elk met de elementen van de Tuples van de invoer matrix.</span><span class="sxs-lookup"><span data-stu-id="df705-105">Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.</span></span>

```qsharp
function Unzipped<'T, 'U> (arr : ('T, 'U)[]) : ('T[], 'U[])
```


## <a name="input"></a><span data-ttu-id="df705-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="df705-106">Input</span></span>

### <a name="arr--tu"></a><span data-ttu-id="df705-107">ARR: ('T, ' U) []</span><span class="sxs-lookup"><span data-stu-id="df705-107">arr : ('T,'U)[]</span></span>

<span data-ttu-id="df705-108">Een matrix met 2-Tuples</span><span class="sxs-lookup"><span data-stu-id="df705-108">An array containing 2-tuples</span></span>



## <a name="output--tu"></a><span data-ttu-id="df705-109">Uitvoer: ('T [], ' U [])</span><span class="sxs-lookup"><span data-stu-id="df705-109">Output : ('T[],'U[])</span></span>

<span data-ttu-id="df705-110">Twee matrices, de eerste die alle eerste elementen van de ingevoerde Tuples bevat, de tweede matrix met alle tweede elementen van de ingevoerde Tuples.</span><span class="sxs-lookup"><span data-stu-id="df705-110">Two arrays, the first one containing all first elements of the input tuples, the second one containing all second elements of the input tuples.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="df705-111">Type parameters</span><span class="sxs-lookup"><span data-stu-id="df705-111">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="df705-112">T</span><span class="sxs-lookup"><span data-stu-id="df705-112">'T</span></span>

<span data-ttu-id="df705-113">Het type van het eerste element in elke tupel</span><span class="sxs-lookup"><span data-stu-id="df705-113">The type of the first element in each tuple</span></span>
### <a name="u"></a><span data-ttu-id="df705-114">' U</span><span class="sxs-lookup"><span data-stu-id="df705-114">'U</span></span>

<span data-ttu-id="df705-115">Het type van het tweede element in elke tupel</span><span class="sxs-lookup"><span data-stu-id="df705-115">The type of the second element in each tuple</span></span>

## <a name="example"></a><span data-ttu-id="df705-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="df705-116">Example</span></span>

```qsharp
// split is same as ([6, 5, 5, 3, 2, 1], [true, false, false, false, true, false])
let split = Unzipped([(6, true), (5, false), (5, false), (3, false), (2, true), (1, false)]);
```

## <a name="see-also"></a><span data-ttu-id="df705-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="df705-117">See Also</span></span>

- [<span data-ttu-id="df705-118">Microsoft.Quantum.Arrays.ZipPED</span><span class="sxs-lookup"><span data-stu-id="df705-118">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)