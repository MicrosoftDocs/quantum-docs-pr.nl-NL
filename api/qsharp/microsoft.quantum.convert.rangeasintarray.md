---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: De functie RangeAsIntArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: bd3ac51d2925d7a4450b2bc5e6f7899fcab18f2c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702921"
---
# <a name="rangeasintarray-function"></a><span data-ttu-id="220c9-102">De functie RangeAsIntArray</span><span class="sxs-lookup"><span data-stu-id="220c9-102">RangeAsIntArray function</span></span>

<span data-ttu-id="220c9-103">Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)</span><span class="sxs-lookup"><span data-stu-id="220c9-103">Namespace: [Microsoft.Quantum.Convert](xref:Microsoft.Quantum.Convert)</span></span>

<span data-ttu-id="220c9-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="220c9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="220c9-105">Maakt een matrix `arr` met gehele getallen die worden opgesomd door start.. stap.. endsystemen.</span><span class="sxs-lookup"><span data-stu-id="220c9-105">Creates an array `arr` of integers enumerated by start..step..end.</span></span>

```qsharp
function RangeAsIntArray (range : Range) : Int[]
```


## <a name="input"></a><span data-ttu-id="220c9-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="220c9-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="220c9-107">bereik: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="220c9-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>

<span data-ttu-id="220c9-108">Een `Range` van de waarden `start..step..end` die moeten worden geconverteerd naar een matrix.</span><span class="sxs-lookup"><span data-stu-id="220c9-108">A `Range` of values `start..step..end` to be converted to an array.</span></span>



## <a name="output--int"></a><span data-ttu-id="220c9-109">Output: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="220c9-109">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="220c9-110">Een nieuwe matrix van gehele getallen die overeenkomen met waarden die worden herhaald door `range` .</span><span class="sxs-lookup"><span data-stu-id="220c9-110">A new array of integers corresponding to values iterated over by `range`.</span></span>