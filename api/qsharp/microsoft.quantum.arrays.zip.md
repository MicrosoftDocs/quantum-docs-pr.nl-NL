---
uid: Microsoft.Quantum.Arrays.Zip
title: Zip-functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip
qsharp.summary: >-
  > [!WARNING]

  > Zip has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.


  Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 32fea60fc36bfdbaa2ab2f3560f291bf4ce4fa51
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705684"
---
# <a name="zip-function"></a><span data-ttu-id="1eda5-102">Zip-functie</span><span class="sxs-lookup"><span data-stu-id="1eda5-102">Zip function</span></span>

<span data-ttu-id="1eda5-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="1eda5-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="1eda5-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1eda5-104">Package: [](https://nuget.org/packages/)</span></span>


> [!WARNING]
> <span data-ttu-id="1eda5-105">Zip is afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="1eda5-105">Zip has been deprecated.</span></span> <span data-ttu-id="1eda5-106">Gebruik <xref:Microsoft.Quantum.Arrays.Zipped> in plaats daarvan.</span><span class="sxs-lookup"><span data-stu-id="1eda5-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.</span></span>

<span data-ttu-id="1eda5-107">Als er twee matrices worden opgegeven, wordt er een nieuwe matrix van paren geretourneerd, zodat elk paar een element uit elke oorspronkelijke matrix bevat.</span><span class="sxs-lookup"><span data-stu-id="1eda5-107">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zip<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="1eda5-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="1eda5-108">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="1eda5-109">links: ' []</span><span class="sxs-lookup"><span data-stu-id="1eda5-109">left : 'T[]</span></span>

<span data-ttu-id="1eda5-110">Een matrix met waarden voor het eerste element van elke tuple.</span><span class="sxs-lookup"><span data-stu-id="1eda5-110">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="1eda5-111">rechts: ' U []</span><span class="sxs-lookup"><span data-stu-id="1eda5-111">right : 'U[]</span></span>

<span data-ttu-id="1eda5-112">Een matrix met waarden voor het tweede element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="1eda5-112">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="1eda5-113">Uitvoer: ('T, ' U) []</span><span class="sxs-lookup"><span data-stu-id="1eda5-113">Output : ('T,'U)[]</span></span>

<span data-ttu-id="1eda5-114">Een matrix die de paren van het formulier bevat `(left[idx], right[idx])` `idx` .</span><span class="sxs-lookup"><span data-stu-id="1eda5-114">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="1eda5-115">Als de twee matrices een lengte hebben die niet even groot is, is de uitvoer zo lang als de kortste van de invoer.</span><span class="sxs-lookup"><span data-stu-id="1eda5-115">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="1eda5-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="1eda5-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1eda5-117">T</span><span class="sxs-lookup"><span data-stu-id="1eda5-117">'T</span></span>

<span data-ttu-id="1eda5-118">Het type van de elementen van de linker matrix.</span><span class="sxs-lookup"><span data-stu-id="1eda5-118">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="1eda5-119">' U</span><span class="sxs-lookup"><span data-stu-id="1eda5-119">'U</span></span>

<span data-ttu-id="1eda5-120">Het type van de rechter matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="1eda5-120">The type of the right array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="1eda5-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1eda5-121">See Also</span></span>

- [<span data-ttu-id="1eda5-122">Microsoft.Quantum.Arrays.Zip3</span><span class="sxs-lookup"><span data-stu-id="1eda5-122">Microsoft.Quantum.Arrays.Zip3</span></span>](xref:Microsoft.Quantum.Arrays.Zip3)
- [<span data-ttu-id="1eda5-123">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="1eda5-123">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)
- [<span data-ttu-id="1eda5-124">Micro soft. Quantum. arrays. ungezipte</span><span class="sxs-lookup"><span data-stu-id="1eda5-124">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)