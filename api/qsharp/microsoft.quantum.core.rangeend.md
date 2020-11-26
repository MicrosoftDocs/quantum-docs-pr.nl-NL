---
uid: Microsoft.Quantum.Core.RangeEnd
title: De functie RangeEnd
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeEnd
qsharp.summary: Returns the defined end value of the given range, which is not necessarily the last element in the sequence.
ms.openlocfilehash: 90a9e31bf5c4a5e92a35998ddaec8c9e9de9888e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224034"
---
# <a name="rangeend-function"></a><span data-ttu-id="a1758-102">De functie RangeEnd</span><span class="sxs-lookup"><span data-stu-id="a1758-102">RangeEnd function</span></span>

<span data-ttu-id="a1758-103">Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="a1758-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="a1758-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="a1758-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="a1758-105">Retourneert de gedefinieerde eind waarde van het opgegeven bereik. Dit is niet noodzakelijkerwijs het laatste element in de reeks.</span><span class="sxs-lookup"><span data-stu-id="a1758-105">Returns the defined end value of the given range, which is not necessarily the last element in the sequence.</span></span>

```qsharp
function RangeEnd (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="a1758-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a1758-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="a1758-107">bereik: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="a1758-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="a1758-108">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a1758-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a1758-109">De gedefinieerde eind waarde van het opgegeven bereik.</span><span class="sxs-lookup"><span data-stu-id="a1758-109">The defined end value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1758-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="a1758-110">Remarks</span></span>

<span data-ttu-id="a1758-111">Het eerste element van een bereik expressie is `start` , het tweede element is, het `start+step` derde element `start+step+step` , enzovoort, totdat het `end` wordt door gegeven.</span><span class="sxs-lookup"><span data-stu-id="a1758-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="a1758-112">Houd er rekening mee dat de gedefinieerde eind waarde van een bereik kan verschillen van het laatste element in de reeks die is opgegeven door het bereik. bijvoorbeeld in een bereik van 0..</span><span class="sxs-lookup"><span data-stu-id="a1758-112">Note that the defined end value of a range can differ from the last element in the sequence specified by the range; for example, in a range 0 ..</span></span> <span data-ttu-id="a1758-113">2..</span><span class="sxs-lookup"><span data-stu-id="a1758-113">2 ..</span></span> <span data-ttu-id="a1758-114">5 het laatste element is 4, maar de eind waarde is 5.</span><span class="sxs-lookup"><span data-stu-id="a1758-114">5 the last element is 4 but the end value is 5.</span></span>