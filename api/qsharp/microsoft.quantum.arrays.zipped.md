---
uid: Microsoft.Quantum.Arrays.Zipped
title: Gezipte functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped
qsharp.summary: Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 56ed97d573bf29dddb7cdb1c3f360218bf97889a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219750"
---
# <a name="zipped-function"></a><span data-ttu-id="db7db-102">Gezipte functie</span><span class="sxs-lookup"><span data-stu-id="db7db-102">Zipped function</span></span>

<span data-ttu-id="db7db-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="db7db-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="db7db-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="db7db-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="db7db-105">Als er twee matrices worden opgegeven, wordt er een nieuwe matrix van paren geretourneerd, zodat elk paar een element uit elke oorspronkelijke matrix bevat.</span><span class="sxs-lookup"><span data-stu-id="db7db-105">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zipped<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="db7db-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="db7db-106">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="db7db-107">links: ' []</span><span class="sxs-lookup"><span data-stu-id="db7db-107">left : 'T[]</span></span>

<span data-ttu-id="db7db-108">Een matrix met waarden voor het eerste element van elke tuple.</span><span class="sxs-lookup"><span data-stu-id="db7db-108">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="db7db-109">rechts: ' U []</span><span class="sxs-lookup"><span data-stu-id="db7db-109">right : 'U[]</span></span>

<span data-ttu-id="db7db-110">Een matrix met waarden voor het tweede element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="db7db-110">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="db7db-111">Uitvoer: ('T, ' U) []</span><span class="sxs-lookup"><span data-stu-id="db7db-111">Output : ('T,'U)[]</span></span>

<span data-ttu-id="db7db-112">Een matrix die de paren van het formulier bevat `(left[idx], right[idx])` `idx` .</span><span class="sxs-lookup"><span data-stu-id="db7db-112">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="db7db-113">Als de twee matrices een lengte hebben die niet even groot is, is de uitvoer zo lang als de kortste van de invoer.</span><span class="sxs-lookup"><span data-stu-id="db7db-113">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="db7db-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="db7db-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="db7db-115">T</span><span class="sxs-lookup"><span data-stu-id="db7db-115">'T</span></span>

<span data-ttu-id="db7db-116">Het type van de elementen van de linker matrix.</span><span class="sxs-lookup"><span data-stu-id="db7db-116">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="db7db-117">' U</span><span class="sxs-lookup"><span data-stu-id="db7db-117">'U</span></span>

<span data-ttu-id="db7db-118">Het type van de rechter matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="db7db-118">The type of the right array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="db7db-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="db7db-119">See Also</span></span>

- [<span data-ttu-id="db7db-120">Microsoft.Quantum.Arrays.ZipPED3</span><span class="sxs-lookup"><span data-stu-id="db7db-120">Microsoft.Quantum.Arrays.Zipped3</span></span>](xref:Microsoft.Quantum.Arrays.Zipped3)
- [<span data-ttu-id="db7db-121">Microsoft.Quantum.Arrays.Zipped4</span><span class="sxs-lookup"><span data-stu-id="db7db-121">Microsoft.Quantum.Arrays.Zipped4</span></span>](xref:Microsoft.Quantum.Arrays.Zipped4)
- [<span data-ttu-id="db7db-122">Micro soft. Quantum. arrays. ungezipte</span><span class="sxs-lookup"><span data-stu-id="db7db-122">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)