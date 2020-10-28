---
uid: Microsoft.Quantum.Core.RangeEnd
title: De functie RangeEnd
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 4dbcf517c4dc17775040444c77deb0e449082390
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702872"
---
# <a name="rangeend-function"></a><span data-ttu-id="dc95a-102">De functie RangeEnd</span><span class="sxs-lookup"><span data-stu-id="dc95a-102">RangeEnd function</span></span>

<span data-ttu-id="dc95a-103">Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="dc95a-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="dc95a-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="dc95a-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="dc95a-105">Retourneert de gedefinieerde eind waarde van het opgegeven bereik. Dit is niet noodzakelijkerwijs het laatste element in de reeks.</span><span class="sxs-lookup"><span data-stu-id="dc95a-105">Returns the defined end value of the given range, which is not necessarily the last element in the sequence.</span></span>

```qsharp
function RangeEnd (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="dc95a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="dc95a-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="dc95a-107">bereik: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="dc95a-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="dc95a-108">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="dc95a-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="dc95a-109">De gedefinieerde eind waarde van het opgegeven bereik.</span><span class="sxs-lookup"><span data-stu-id="dc95a-109">The defined end value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc95a-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="dc95a-110">Remarks</span></span>

<span data-ttu-id="dc95a-111">Het eerste element van een bereik expressie is `start` , het tweede element is, het `start+step` derde element `start+step+step` , enzovoort, totdat het `end` wordt door gegeven.</span><span class="sxs-lookup"><span data-stu-id="dc95a-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="dc95a-112">Houd er rekening mee dat de gedefinieerde eind waarde van een bereik kan verschillen van het laatste element in de reeks die is opgegeven door het bereik. bijvoorbeeld in een bereik van 0..</span><span class="sxs-lookup"><span data-stu-id="dc95a-112">Note that the defined end value of a range can differ from the last element in the sequence specified by the range; for example, in a range 0 ..</span></span> <span data-ttu-id="dc95a-113">2..</span><span class="sxs-lookup"><span data-stu-id="dc95a-113">2 ..</span></span> <span data-ttu-id="dc95a-114">5 het laatste element is 4, maar de eind waarde is 5.</span><span class="sxs-lookup"><span data-stu-id="dc95a-114">5 the last element is 4 but the end value is 5.</span></span>