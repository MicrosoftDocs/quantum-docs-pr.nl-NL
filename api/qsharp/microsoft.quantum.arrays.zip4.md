---
uid: Microsoft.Quantum.Arrays.Zip4
title: De functie Zip4
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip4
qsharp.summary: >-
  > [!WARNING]

  > Zip4 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped4> instead.


  Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: d42b3b6db059163f6c766d4f133551be293c153d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705661"
---
# <a name="zip4-function"></a><span data-ttu-id="7793e-102">De functie Zip4</span><span class="sxs-lookup"><span data-stu-id="7793e-102">Zip4 function</span></span>

<span data-ttu-id="7793e-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7793e-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7793e-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="7793e-104">Package: [](https://nuget.org/packages/)</span></span>


> [!WARNING]
> <span data-ttu-id="7793e-105">Zip4 is afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="7793e-105">Zip4 has been deprecated.</span></span> <span data-ttu-id="7793e-106">Gebruik <xref:Microsoft.Quantum.Arrays.Zipped4> in plaats daarvan.</span><span class="sxs-lookup"><span data-stu-id="7793e-106">Please use <xref:Microsoft.Quantum.Arrays.Zipped4> instead.</span></span>

<span data-ttu-id="7793e-107">Gegeven vier matrices retourneert een nieuwe matrix van 4 Tuples, zodat elke 4-tuple een element uit elke oorspronkelijke matrix bevat.</span><span class="sxs-lookup"><span data-stu-id="7793e-107">Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.</span></span>

```qsharp
function Zip4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
```


## <a name="input"></a><span data-ttu-id="7793e-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="7793e-108">Input</span></span>

### <a name="first--t1"></a><span data-ttu-id="7793e-109">eerst: 'T 1 []</span><span class="sxs-lookup"><span data-stu-id="7793e-109">first : 'T1[]</span></span>

<span data-ttu-id="7793e-110">Een matrix met waarden voor het eerste element van elke tuple.</span><span class="sxs-lookup"><span data-stu-id="7793e-110">An array containing values for the first element of each tuple.</span></span>


### <a name="second--t2"></a><span data-ttu-id="7793e-111">seconde: 'T 2 []</span><span class="sxs-lookup"><span data-stu-id="7793e-111">second : 'T2[]</span></span>

<span data-ttu-id="7793e-112">Een matrix met waarden voor het tweede element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="7793e-112">An array containing values for the second element of each tuple.</span></span>


### <a name="third--t3"></a><span data-ttu-id="7793e-113">derde: 'T 3 []</span><span class="sxs-lookup"><span data-stu-id="7793e-113">third : 'T3[]</span></span>

<span data-ttu-id="7793e-114">Een matrix met waarden voor het derde element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="7793e-114">An array containing values for the third element of each tuple.</span></span>


### <a name="fourth--t4"></a><span data-ttu-id="7793e-115">vierde: 'T 4 []</span><span class="sxs-lookup"><span data-stu-id="7793e-115">fourth : 'T4[]</span></span>

<span data-ttu-id="7793e-116">Een matrix met waarden voor het vierde element van elke tupel.</span><span class="sxs-lookup"><span data-stu-id="7793e-116">An array containing values for the fourth element of each tuple.</span></span>



## <a name="output--t1t2t3t4"></a><span data-ttu-id="7793e-117">Uitvoer: (niet 1, 'T 2, niet 3, niet 4) []</span><span class="sxs-lookup"><span data-stu-id="7793e-117">Output : ('T1,'T2,'T3,'T4)[]</span></span>

<span data-ttu-id="7793e-118">Een matrix met vier Tuples van het formulier `(first[idx], second[idx], third[idx], fourth[idx])` voor elke `idx` .</span><span class="sxs-lookup"><span data-stu-id="7793e-118">An array containing 4-tuples of the form `(first[idx], second[idx], third[idx], fourth[idx])` for each `idx`.</span></span> <span data-ttu-id="7793e-119">Als de vier matrices een lengte hebben die niet even groot is, is de uitvoer zo lang als de kortste van de invoer.</span><span class="sxs-lookup"><span data-stu-id="7793e-119">If the four arrays are not of equal length, the output will be as long as the shorter of the inputs.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="7793e-120">Type parameters</span><span class="sxs-lookup"><span data-stu-id="7793e-120">Type Parameters</span></span>

### <a name="t1"></a><span data-ttu-id="7793e-121">Niet 1</span><span class="sxs-lookup"><span data-stu-id="7793e-121">'T1</span></span>

<span data-ttu-id="7793e-122">Het type van de eerste matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="7793e-122">The type of the first array elements.</span></span>
### <a name="t2"></a><span data-ttu-id="7793e-123">Niet 2</span><span class="sxs-lookup"><span data-stu-id="7793e-123">'T2</span></span>

<span data-ttu-id="7793e-124">Het type van de tweede matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="7793e-124">The type of the second array elements.</span></span>
### <a name="t3"></a><span data-ttu-id="7793e-125">Niet 3</span><span class="sxs-lookup"><span data-stu-id="7793e-125">'T3</span></span>

<span data-ttu-id="7793e-126">Het type van de derde matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="7793e-126">The type of the third array elements.</span></span>
### <a name="t4"></a><span data-ttu-id="7793e-127">Niet 4</span><span class="sxs-lookup"><span data-stu-id="7793e-127">'T4</span></span>

<span data-ttu-id="7793e-128">Het type van de vierde matrix elementen.</span><span class="sxs-lookup"><span data-stu-id="7793e-128">The type of the fourth array elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="7793e-129">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7793e-129">See Also</span></span>

- [<span data-ttu-id="7793e-130">Microsoft.Quantum.Arrays.Zip</span><span class="sxs-lookup"><span data-stu-id="7793e-130">Microsoft.Quantum.Arrays.Zip</span></span>](xref:Microsoft.Quantum.Arrays.Zip)
- [<span data-ttu-id="7793e-131">Microsoft.Quantum.Arrays.Zip3</span><span class="sxs-lookup"><span data-stu-id="7793e-131">Microsoft.Quantum.Arrays.Zip3</span></span>](xref:Microsoft.Quantum.Arrays.Zip3)