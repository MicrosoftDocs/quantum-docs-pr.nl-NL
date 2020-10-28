---
uid: Microsoft.Quantum.Arrays.Zipped4
title: De functie Zipped4
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped4
qsharp.summary: Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: 413b415288170b4a6bffbb773e3277cdb47bdbbe
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705652"
---
# <a name="zipped4-function"></a><span data-ttu-id="3716f-102">De functie Zipped4</span><span class="sxs-lookup"><span data-stu-id="3716f-102">Zipped4 function</span></span>

<span data-ttu-id="3716f-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3716f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3716f-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3716f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3716f-105">Gegeven vier matrices retourneert een nieuwe matrix van 4 Tuples, zodat elke 4-tuple een element uit elke oorspronkelijke matrix bevat.</span><span class="sxs-lookup"><span data-stu-id="3716f-105">Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.</span></span>

```qsharp
function Zipped4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
```


## <a name="input"></a><span data-ttu-id="3716f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="3716f-106">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="3716f-107">eerst: 'T 1 []</span><span class="sxs-lookup"><span data-stu-id="3716f-107">first : 'T1[]</span></span>

<span data-ttu-id="3716f-108">Een matrix met waarden voor het eerste element van elke tuple.</span><span class="sxs-lookup"><span data-stu-id="3716f-108">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="3716f-109">seconde: 'T 2 []</span><span class="sxs-lookup"><span data-stu-id="3716f-109">second : 'T2[]</span></span>

<span data-ttu-id="3716f-110">Een matrix met waarden voor het tweede element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="3716f-110">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="3716f-111">derde: 'T 3 []</span><span class="sxs-lookup"><span data-stu-id="3716f-111">third : 'T3[]</span></span>

<span data-ttu-id="3716f-112">Een matrix met waarden voor het derde element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="3716f-112">An array containing values for the third element of each tuple.</span></span>


### <a name="fourth--t4"></a><span data-ttu-id="3716f-113">vierde: 'T 4 []</span><span class="sxs-lookup"><span data-stu-id="3716f-113">fourth : 'T4[]</span></span>

<span data-ttu-id="3716f-114">Een matrix met waarden voor het vierde element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="3716f-114">An array containing values for the fourth element of each tuple.</span></span>



## <a name="output--t1t2t3t4"></a><span data-ttu-id="3716f-115">Uitvoer: (niet 1, 'T 2, niet 3, niet 4) []</span><span class="sxs-lookup"><span data-stu-id="3716f-115">Output : ('T1,'T2,'T3,'T4)[]</span></span>

<span data-ttu-id="3716f-116">Een matrix met vier Tuples van het formulier `(first[idx], second[idx], third[idx], fourth[idx])` voor elke `idx` .</span><span class="sxs-lookup"><span data-stu-id="3716f-116">An array containing 4-tuples of the form `(first[idx], second[idx], third[idx], fourth[idx])` for each `idx`.</span></span> <span data-ttu-id="3716f-117">Als de vier matrices een lengte hebben die niet even groot is, is de uitvoer zo lang als de kortste van de invoer.</span><span class="sxs-lookup"><span data-stu-id="3716f-117">If the four arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="3716f-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="3716f-118">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="3716f-119">Niet 1</span><span class="sxs-lookup"><span data-stu-id="3716f-119">'T1</span></span>

<span data-ttu-id="3716f-120">Het type van de eerste matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="3716f-120">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="3716f-121">Niet 2</span><span class="sxs-lookup"><span data-stu-id="3716f-121">'T2</span></span>

<span data-ttu-id="3716f-122">Het type van de tweede matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="3716f-122">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="3716f-123">Niet 3</span><span class="sxs-lookup"><span data-stu-id="3716f-123">'T3</span></span>

<span data-ttu-id="3716f-124">Het type van de derde matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="3716f-124">The type of the third array elements.</span></span>
### <a name="t4"></a><span data-ttu-id="3716f-125">Niet 4</span><span class="sxs-lookup"><span data-stu-id="3716f-125">'T4</span></span>

<span data-ttu-id="3716f-126">Het type van de vierde matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="3716f-126">The type of the fourth array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="3716f-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3716f-127">See Also</span></span>

- [<span data-ttu-id="3716f-128">Microsoft.Quantum.Arrays.ZipPED</span><span class="sxs-lookup"><span data-stu-id="3716f-128">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)
- [<span data-ttu-id="3716f-129">Microsoft.Quantum.Arrays.ZipPED3</span><span class="sxs-lookup"><span data-stu-id="3716f-129">Microsoft.Quantum.Arrays.Zipped3</span></span>](xref:Microsoft.Quantum.Arrays.Zipped3)