---
uid: Microsoft.Quantum.Arrays.ElementAt
title: De functie ElementAt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ElementAt
qsharp.summary: Returns the at the given index of an array.
ms.openlocfilehash: 2d31c62a4a5ba3b273e7440b5dfe4482b47e3a8b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842805"
---
# <a name="elementat-function"></a><span data-ttu-id="2ac10-102">De functie ElementAt</span><span class="sxs-lookup"><span data-stu-id="2ac10-102">ElementAt function</span></span>

<span data-ttu-id="2ac10-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2ac10-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2ac10-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2ac10-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2ac10-105">Retourneert de opgegeven index van een matrix.</span><span class="sxs-lookup"><span data-stu-id="2ac10-105">Returns the at the given index of an array.</span></span>

```qsharp
function ElementAt<'T> (index : Int, array : 'T[]) : 'T
```


## <a name="input"></a><span data-ttu-id="2ac10-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="2ac10-106">Input</span></span>

### <a name="index--int"></a><span data-ttu-id="2ac10-107">index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2ac10-107">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2ac10-108">Index van element</span><span class="sxs-lookup"><span data-stu-id="2ac10-108">Index of element</span></span>


### <a name="array--t"></a><span data-ttu-id="2ac10-109">matrix: 'T []</span><span class="sxs-lookup"><span data-stu-id="2ac10-109">array : 'T[]</span></span>

<span data-ttu-id="2ac10-110">De matrix die wordt geïndexeerd.</span><span class="sxs-lookup"><span data-stu-id="2ac10-110">The array being indexed.</span></span>



## <a name="output--t"></a><span data-ttu-id="2ac10-111">Uitvoer: 'T</span><span class="sxs-lookup"><span data-stu-id="2ac10-111">Output : 'T</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2ac10-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="2ac10-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2ac10-113">T</span><span class="sxs-lookup"><span data-stu-id="2ac10-113">'T</span></span>

<span data-ttu-id="2ac10-114">Het type van elk element van `array` .</span><span class="sxs-lookup"><span data-stu-id="2ac10-114">The type of each element of `array`.</span></span>

## <a name="example"></a><span data-ttu-id="2ac10-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="2ac10-115">Example</span></span>

<span data-ttu-id="2ac10-116">Haal het derde getal op in vier beroemde gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="2ac10-116">Get the third number in four famous integer sequences.</span></span> <span data-ttu-id="2ac10-117">(Houd er rekening mee dat de 0-index overeenkomt met de _eerste_ waarde van de reeks.)</span><span class="sxs-lookup"><span data-stu-id="2ac10-117">(note that the 0 index corresponds to the _first_ value of the sequence.)</span></span>

```qsharp
let lucas = [2, 1, 3, 4, 7, 11, 18, 29, 47, 76];
let prime = [2, 3, 5, 7, 11, 13, 17, 19, 23, 29];
let fibonacci = [0, 1, 1, 2, 3, 5, 8, 13, 21, 34];
let catalan = [1, 1, 2, 5, 14, 42, 132, 429, 1430, 4862];
let famous2 = Mapped(ElementAt<Int>(2, _), [lucas, prime, fibonacci, catalan]);
// same as: famous2 = [3, 5, 1, 2]
```

## <a name="see-also"></a><span data-ttu-id="2ac10-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2ac10-118">See Also</span></span>

- [<span data-ttu-id="2ac10-119">Micro soft. Quantum. arrays. LookupFunction</span><span class="sxs-lookup"><span data-stu-id="2ac10-119">Microsoft.Quantum.Arrays.LookupFunction</span></span>](xref:Microsoft.Quantum.Arrays.LookupFunction)
- [<span data-ttu-id="2ac10-120">Micro soft. Quantum. arrays. ElementsAt</span><span class="sxs-lookup"><span data-stu-id="2ac10-120">Microsoft.Quantum.Arrays.ElementsAt</span></span>](xref:Microsoft.Quantum.Arrays.ElementsAt)