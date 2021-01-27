---
uid: Microsoft.Quantum.Arrays.Zipped4
title: De functie Zipped4
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped4
qsharp.summary: Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: e932cd4c266b39a3a88da48e649448d0028f61e3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845318"
---
# <a name="zipped4-function"></a><span data-ttu-id="d590e-102">De functie Zipped4</span><span class="sxs-lookup"><span data-stu-id="d590e-102">Zipped4 function</span></span>

<span data-ttu-id="d590e-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="d590e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="d590e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d590e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d590e-105">Gegeven vier matrices retourneert een nieuwe matrix van 4 Tuples, zodat elke 4-tuple een element uit elke oorspronkelijke matrix bevat.</span><span class="sxs-lookup"><span data-stu-id="d590e-105">Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.</span></span>

```qsharp
function Zipped4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
```


## <a name="input"></a><span data-ttu-id="d590e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d590e-106">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="d590e-107">eerst: 'T 1 []</span><span class="sxs-lookup"><span data-stu-id="d590e-107">first : 'T1[]</span></span>

<span data-ttu-id="d590e-108">Een matrix met waarden voor het eerste element van elke tuple.</span><span class="sxs-lookup"><span data-stu-id="d590e-108">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="d590e-109">seconde: 'T 2 []</span><span class="sxs-lookup"><span data-stu-id="d590e-109">second : 'T2[]</span></span>

<span data-ttu-id="d590e-110">Een matrix met waarden voor het tweede element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="d590e-110">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="d590e-111">derde: 'T 3 []</span><span class="sxs-lookup"><span data-stu-id="d590e-111">third : 'T3[]</span></span>

<span data-ttu-id="d590e-112">Een matrix met waarden voor het derde element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="d590e-112">An array containing values for the third element of each tuple.</span></span>


### <a name="fourth--t4"></a><span data-ttu-id="d590e-113">vierde: 'T 4 []</span><span class="sxs-lookup"><span data-stu-id="d590e-113">fourth : 'T4[]</span></span>

<span data-ttu-id="d590e-114">Een matrix met waarden voor het vierde element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="d590e-114">An array containing values for the fourth element of each tuple.</span></span>



## <a name="output--t1t2t3t4"></a><span data-ttu-id="d590e-115">Uitvoer: (niet 1, 'T 2, niet 3, niet 4) []</span><span class="sxs-lookup"><span data-stu-id="d590e-115">Output : ('T1,'T2,'T3,'T4)[]</span></span>

<span data-ttu-id="d590e-116">Een matrix met vier Tuples van het formulier `(first[idx], second[idx], third[idx], fourth[idx])` voor elke `idx` .</span><span class="sxs-lookup"><span data-stu-id="d590e-116">An array containing 4-tuples of the form `(first[idx], second[idx], third[idx], fourth[idx])` for each `idx`.</span></span> <span data-ttu-id="d590e-117">Als de vier matrices een lengte hebben die niet even groot is, is de uitvoer zo lang als de kortste van de invoer.</span><span class="sxs-lookup"><span data-stu-id="d590e-117">If the four arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="d590e-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d590e-118">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="d590e-119">Niet 1</span><span class="sxs-lookup"><span data-stu-id="d590e-119">'T1</span></span>

<span data-ttu-id="d590e-120">Het type van de eerste matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="d590e-120">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="d590e-121">Niet 2</span><span class="sxs-lookup"><span data-stu-id="d590e-121">'T2</span></span>

<span data-ttu-id="d590e-122">Het type van de tweede matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="d590e-122">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="d590e-123">Niet 3</span><span class="sxs-lookup"><span data-stu-id="d590e-123">'T3</span></span>

<span data-ttu-id="d590e-124">Het type van de derde matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="d590e-124">The type of the third array elements.</span></span>
### <a name="t4"></a><span data-ttu-id="d590e-125">Niet 4</span><span class="sxs-lookup"><span data-stu-id="d590e-125">'T4</span></span>

<span data-ttu-id="d590e-126">Het type van de vierde matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="d590e-126">The type of the fourth array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="d590e-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d590e-127">See Also</span></span>

- [<span data-ttu-id="d590e-128">Microsoft.Quantum.Arrays.ZipPED</span><span class="sxs-lookup"><span data-stu-id="d590e-128">Microsoft.Quantum.Arrays.Zipped</span></span>](xref:Microsoft.Quantum.Arrays.Zipped)
- [<span data-ttu-id="d590e-129">Microsoft.Quantum.Arrays.ZipPED3</span><span class="sxs-lookup"><span data-stu-id="d590e-129">Microsoft.Quantum.Arrays.Zipped3</span></span>](xref:Microsoft.Quantum.Arrays.Zipped3)