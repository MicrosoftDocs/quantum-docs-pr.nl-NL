---
uid: Microsoft.Quantum.Arrays.Zip3
title: De functie Zip3
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip3
qsharp.summary: >-
  > [!WARNING]

  > Zip3 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped3> instead.


  Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: f4b1a769614ee9434b2141b8fcb91f34cd071bdb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705677"
---
# <a name="zip3-function"></a><span data-ttu-id="44acb-102">De functie Zip3</span><span class="sxs-lookup"><span data-stu-id="44acb-102">Zip3 function</span></span>

<span data-ttu-id="44acb-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="44acb-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="44acb-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="44acb-104">Package: [](https://nuget.org/packages/)</span></span>


> [!WARNING]
> <span data-ttu-id="44acb-105">Zip3 is afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="44acb-105">Zip3 has been deprecated.</span></span> <span data-ttu-id="44acb-106">Gebruik <xref:Microsoft.Quantum.Arrays.Zipped3> in plaats daarvan.</span><span class="sxs-lookup"><span data-stu-id="44acb-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped3> instead.</span></span>

<span data-ttu-id="44acb-107">Als er drie matrices zijn opgegeven, wordt een nieuwe matrix van 3-Tuples geretourneerd, zodat elke 3-tuple een element uit elke oorspronkelijke matrix bevat.</span><span class="sxs-lookup"><span data-stu-id="44acb-107">Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.</span></span>

```qsharp
function Zip3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a><span data-ttu-id="44acb-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="44acb-108">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="44acb-109">eerst: 'T 1 []</span><span class="sxs-lookup"><span data-stu-id="44acb-109">first : 'T1[]</span></span>

<span data-ttu-id="44acb-110">Een matrix met waarden voor het eerste element van elke tuple.</span><span class="sxs-lookup"><span data-stu-id="44acb-110">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="44acb-111">seconde: 'T 2 []</span><span class="sxs-lookup"><span data-stu-id="44acb-111">second : 'T2[]</span></span>

<span data-ttu-id="44acb-112">Een matrix met waarden voor het tweede element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="44acb-112">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="44acb-113">derde: 'T 3 []</span><span class="sxs-lookup"><span data-stu-id="44acb-113">third : 'T3[]</span></span>

<span data-ttu-id="44acb-114">Een matrix met waarden voor het derde element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="44acb-114">An array containing values for the third element of each tuple.</span></span>



## <a name="output--t1t2t3"></a><span data-ttu-id="44acb-115">Uitvoer: (niet 1, niet 2, niet 3) []</span><span class="sxs-lookup"><span data-stu-id="44acb-115">Output : ('T1,'T2,'T3)[]</span></span>

<span data-ttu-id="44acb-116">Een matrix met drie Tuples van het formulier `(first[idx], second[idx], third[idx])` voor elke `idx` .</span><span class="sxs-lookup"><span data-stu-id="44acb-116">An array containing 3-tuples of the form `(first[idx], second[idx], third[idx])` for each `idx`.</span></span> <span data-ttu-id="44acb-117">Als de drie matrices een lengte hebben die niet even groot is, is de uitvoer zo lang als de kortste van de invoer.</span><span class="sxs-lookup"><span data-stu-id="44acb-117">If the three arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="44acb-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="44acb-118">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="44acb-119">Niet 1</span><span class="sxs-lookup"><span data-stu-id="44acb-119">'T1</span></span>

<span data-ttu-id="44acb-120">Het type van de eerste matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="44acb-120">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="44acb-121">Niet 2</span><span class="sxs-lookup"><span data-stu-id="44acb-121">'T2</span></span>

<span data-ttu-id="44acb-122">Het type van de tweede matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="44acb-122">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="44acb-123">Niet 3</span><span class="sxs-lookup"><span data-stu-id="44acb-123">'T3</span></span>

<span data-ttu-id="44acb-124">Het type van de derde matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="44acb-124">The type of the third array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="44acb-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="44acb-125">See Also</span></span>

- [<span data-ttu-id="44acb-126">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="44acb-126">Microsoft.Quantum.Arrays.Zip</span></span>](xref:Microsoft.Quantum.Arrays.Zip)
- [<span data-ttu-id="44acb-127">Microsoft.Quantum.Arrays.Zip4</span><span class="sxs-lookup"><span data-stu-id="44acb-127">Microsoft.Quantum.Arrays.Zip4</span></span>](xref:Microsoft.Quantum.Arrays.Zip4)