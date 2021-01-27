---
uid: Microsoft.Quantum.Arrays.Zipped
title: Gezipte functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped
qsharp.summary: Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 5177ab0ade5a9ad7788e60c1028befb84b0191d4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845335"
---
# <a name="zipped-function"></a><span data-ttu-id="77995-102">Gezipte functie</span><span class="sxs-lookup"><span data-stu-id="77995-102">Zipped function</span></span>

<span data-ttu-id="77995-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="77995-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="77995-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="77995-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="77995-105">Als er twee matrices worden opgegeven, wordt er een nieuwe matrix van paren geretourneerd, zodat elk paar een element uit elke oorspronkelijke matrix bevat.</span><span class="sxs-lookup"><span data-stu-id="77995-105">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zipped<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="77995-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="77995-106">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="77995-107">links: ' []</span><span class="sxs-lookup"><span data-stu-id="77995-107">left : 'T[]</span></span>

<span data-ttu-id="77995-108">Een matrix met waarden voor het eerste element van elke tuple.</span><span class="sxs-lookup"><span data-stu-id="77995-108">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="77995-109">rechts: ' U []</span><span class="sxs-lookup"><span data-stu-id="77995-109">right : 'U[]</span></span>

<span data-ttu-id="77995-110">Een matrix met waarden voor het tweede element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="77995-110">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="77995-111">Uitvoer: ('T, ' U) []</span><span class="sxs-lookup"><span data-stu-id="77995-111">Output : ('T,'U)[]</span></span>

<span data-ttu-id="77995-112">Een matrix die de paren van het formulier bevat `(left[idx], right[idx])` `idx` .</span><span class="sxs-lookup"><span data-stu-id="77995-112">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="77995-113">Als de twee matrices een lengte hebben die niet even groot is, is de uitvoer zo lang als de kortste van de invoer.</span><span class="sxs-lookup"><span data-stu-id="77995-113">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="77995-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="77995-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="77995-115">T</span><span class="sxs-lookup"><span data-stu-id="77995-115">'T</span></span>

<span data-ttu-id="77995-116">Het type van de elementen van de linker matrix.</span><span class="sxs-lookup"><span data-stu-id="77995-116">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="77995-117">' U</span><span class="sxs-lookup"><span data-stu-id="77995-117">'U</span></span>

<span data-ttu-id="77995-118">Het type van de rechter matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="77995-118">The type of the right array elements.</span></span>

## <a name="example"></a><span data-ttu-id="77995-119">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="77995-119">Example</span></span>

```qsharp
let left = [1, 3, 71];
let right = [false, true];
let pairs = Zipped(left, right); // [(1, false), (3, true)]
```

## <a name="see-also"></a><span data-ttu-id="77995-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="77995-120">See Also</span></span>

- [<span data-ttu-id="77995-121">Microsoft.Quantum.Arrays.ZipPED3</span><span class="sxs-lookup"><span data-stu-id="77995-121">Microsoft.Quantum.Arrays.Zipped3</span></span>](xref:Microsoft.Quantum.Arrays.Zipped3)
- [<span data-ttu-id="77995-122">Microsoft.Quantum.Arrays.Zipped4</span><span class="sxs-lookup"><span data-stu-id="77995-122">Microsoft.Quantum.Arrays.Zipped4</span></span>](xref:Microsoft.Quantum.Arrays.Zipped4)
- [<span data-ttu-id="77995-123">Micro soft. Quantum. arrays. ungezipte</span><span class="sxs-lookup"><span data-stu-id="77995-123">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)