---
uid: Microsoft.Quantum.Arrays.Zip
title: Zip-functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip
qsharp.summary: >-
  > [!WARNING]

  > Zip has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.


  Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 8ed658003f749efd31b8d841cecbb0a23a471af5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850905"
---
# <a name="zip-function"></a><span data-ttu-id="29222-102">Zip-functie</span><span class="sxs-lookup"><span data-stu-id="29222-102">Zip function</span></span>

<span data-ttu-id="29222-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="29222-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="29222-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="29222-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


> [!WARNING]
> <span data-ttu-id="29222-105">Zip is afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="29222-105">Zip has been deprecated.</span></span> <span data-ttu-id="29222-106">Gebruik <xref:Microsoft.Quantum.Arrays.Zipped> in plaats daarvan.</span><span class="sxs-lookup"><span data-stu-id="29222-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.</span></span>

<span data-ttu-id="29222-107">Als er twee matrices worden opgegeven, wordt er een nieuwe matrix van paren geretourneerd, zodat elk paar een element uit elke oorspronkelijke matrix bevat.</span><span class="sxs-lookup"><span data-stu-id="29222-107">Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.</span></span>

```qsharp
function Zip<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a><span data-ttu-id="29222-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="29222-108">Input</span></span>

### <a name="left--t"></a><span data-ttu-id="29222-109">links: ' []</span><span class="sxs-lookup"><span data-stu-id="29222-109">left : 'T[]</span></span>

<span data-ttu-id="29222-110">Een matrix met waarden voor het eerste element van elke tuple.</span><span class="sxs-lookup"><span data-stu-id="29222-110">An array containing values for the first element of each tuple.</span></span>


### <a name="right--u"></a><span data-ttu-id="29222-111">rechts: ' U []</span><span class="sxs-lookup"><span data-stu-id="29222-111">right : 'U[]</span></span>

<span data-ttu-id="29222-112">Een matrix met waarden voor het tweede element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="29222-112">An array containing values for the second element of each tuple.</span></span>



## <a name="output--tu"></a><span data-ttu-id="29222-113">Uitvoer: ('T, ' U) []</span><span class="sxs-lookup"><span data-stu-id="29222-113">Output : ('T,'U)[]</span></span>

<span data-ttu-id="29222-114">Een matrix die de paren van het formulier bevat `(left[idx], right[idx])` `idx` .</span><span class="sxs-lookup"><span data-stu-id="29222-114">An array containing pairs of the form `(left[idx], right[idx])` for each `idx`.</span></span> <span data-ttu-id="29222-115">Als de twee matrices een lengte hebben die niet even groot is, is de uitvoer zo lang als de kortste van de invoer.</span><span class="sxs-lookup"><span data-stu-id="29222-115">If the two arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="29222-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="29222-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="29222-117">T</span><span class="sxs-lookup"><span data-stu-id="29222-117">'T</span></span>

<span data-ttu-id="29222-118">Het type van de elementen van de linker matrix.</span><span class="sxs-lookup"><span data-stu-id="29222-118">The type of the left array elements.</span></span>
### <a name="u"></a><span data-ttu-id="29222-119">' U</span><span class="sxs-lookup"><span data-stu-id="29222-119">'U</span></span>

<span data-ttu-id="29222-120">Het type van de rechter matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="29222-120">The type of the right array elements.</span></span>

## <a name="example"></a><span data-ttu-id="29222-121">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="29222-121">Example</span></span>

```qsharp
let left = [1, 3, 71];
let right = [false, true];
let pairs = Zip(left, right); // [(1, false), (3, true)]
```

## <a name="see-also"></a><span data-ttu-id="29222-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="29222-122">See Also</span></span>

- [<span data-ttu-id="29222-123">Microsoft.Quantum.Arrays.Zip3</span><span class="sxs-lookup"><span data-stu-id="29222-123">Microsoft.Quantum.Arrays.Zip3</span></span>](xref:Microsoft.Quantum.Arrays.Zip3)
- [<span data-ttu-id="29222-124">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="29222-124">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)
- [<span data-ttu-id="29222-125">Micro soft. Quantum. arrays. ungezipte</span><span class="sxs-lookup"><span data-stu-id="29222-125">Microsoft.Quantum.Arrays.Unzipped</span></span>](xref:Microsoft.Quantum.Arrays.Unzipped)