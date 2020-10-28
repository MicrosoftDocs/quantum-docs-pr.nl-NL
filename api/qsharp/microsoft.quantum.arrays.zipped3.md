---
uid: Microsoft.Quantum.Arrays.Zipped3
title: De functie Zipped3
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped3
qsharp.summary: Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: c0535ca4d6e0de13bf809a21e69d100dcb798d1f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705660"
---
# <a name="zipped3-function"></a><span data-ttu-id="78810-102">De functie Zipped3</span><span class="sxs-lookup"><span data-stu-id="78810-102">Zipped3 function</span></span>

<span data-ttu-id="78810-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="78810-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="78810-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="78810-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="78810-105">Als er drie matrices zijn opgegeven, wordt een nieuwe matrix van 3-Tuples geretourneerd, zodat elke 3-tuple een element uit elke oorspronkelijke matrix bevat.</span><span class="sxs-lookup"><span data-stu-id="78810-105">Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.</span></span>

```qsharp
function Zipped3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a><span data-ttu-id="78810-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="78810-106">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="78810-107">eerst: 'T 1 []</span><span class="sxs-lookup"><span data-stu-id="78810-107">first : 'T1[]</span></span>

<span data-ttu-id="78810-108">Een matrix met waarden voor het eerste element van elke tuple.</span><span class="sxs-lookup"><span data-stu-id="78810-108">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="78810-109">seconde: 'T 2 []</span><span class="sxs-lookup"><span data-stu-id="78810-109">second : 'T2[]</span></span>

<span data-ttu-id="78810-110">Een matrix met waarden voor het tweede element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="78810-110">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="78810-111">derde: 'T 3 []</span><span class="sxs-lookup"><span data-stu-id="78810-111">third : 'T3[]</span></span>

<span data-ttu-id="78810-112">Een matrix met waarden voor het derde element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="78810-112">An array containing values for the third element of each tuple.</span></span>



## <a name="output--t1t2t3"></a><span data-ttu-id="78810-113">Uitvoer: (niet 1, niet 2, niet 3) []</span><span class="sxs-lookup"><span data-stu-id="78810-113">Output : ('T1,'T2,'T3)[]</span></span>

<span data-ttu-id="78810-114">Een matrix met drie Tuples van het formulier `(first[idx], second[idx], third[idx])` voor elke `idx` .</span><span class="sxs-lookup"><span data-stu-id="78810-114">An array containing 3-tuples of the form `(first[idx], second[idx], third[idx])` for each `idx`.</span></span> <span data-ttu-id="78810-115">Als de drie matrices een lengte hebben die niet even groot is, is de uitvoer zo lang als de kortste van de invoer.</span><span class="sxs-lookup"><span data-stu-id="78810-115">If the three arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="78810-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="78810-116">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="78810-117">Niet 1</span><span class="sxs-lookup"><span data-stu-id="78810-117">'T1</span></span>

<span data-ttu-id="78810-118">Het type van de eerste matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="78810-118">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="78810-119">Niet 2</span><span class="sxs-lookup"><span data-stu-id="78810-119">'T2</span></span>

<span data-ttu-id="78810-120">Het type van de tweede matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="78810-120">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="78810-121">Niet 3</span><span class="sxs-lookup"><span data-stu-id="78810-121">'T3</span></span>

<span data-ttu-id="78810-122">Het type van de derde matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="78810-122">The type of the third array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="78810-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="78810-123">See Also</span></span>

- [<span data-ttu-id="78810-124">Microsoft.Quantum.Arrays.ZipPED</span><span class="sxs-lookup"><span data-stu-id="78810-124">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)
- [<span data-ttu-id="78810-125">Microsoft.Quantum.Arrays.Zipped4</span><span class="sxs-lookup"><span data-stu-id="78810-125">Microsoft.Quantum.Arrays.Zipped4</span></span>](xref:Microsoft.Quantum.Arrays.Zipped4)