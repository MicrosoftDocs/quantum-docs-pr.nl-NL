---
uid: Microsoft.Quantum.Core.RangeStep
title: De functie RangeStep
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStep
qsharp.summary: Returns the integer that specifies how the next value of a range is calculated.
ms.openlocfilehash: f8e4c42330f2d6afdc1c0a9bdde36081ccab2f94
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702836"
---
# <a name="rangestep-function"></a><span data-ttu-id="d6472-102">De functie RangeStep</span><span class="sxs-lookup"><span data-stu-id="d6472-102">RangeStep function</span></span>

<span data-ttu-id="d6472-103">Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="d6472-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="d6472-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d6472-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d6472-105">Retourneert het gehele getal dat aangeeft hoe de volgende waarde van een bereik wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="d6472-105">Returns the integer that specifies how the next value of a range is calculated.</span></span>

```qsharp
function RangeStep (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="d6472-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d6472-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="d6472-107">bereik: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="d6472-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="d6472-108">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d6472-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d6472-109">De gedefinieerde stap waarde van het opgegeven bereik.</span><span class="sxs-lookup"><span data-stu-id="d6472-109">The defined step value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6472-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d6472-110">Remarks</span></span>

<span data-ttu-id="d6472-111">Het eerste element van een bereik expressie is `start` , het tweede element is, het `start+step` derde element `start+step+step` , enzovoort, totdat het `end` wordt door gegeven.</span><span class="sxs-lookup"><span data-stu-id="d6472-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>