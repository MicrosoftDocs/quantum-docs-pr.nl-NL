---
uid: Microsoft.Quantum.Core.RangeStart
title: Range Start-functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStart
qsharp.summary: Returns the defined start value of the given range.
ms.openlocfilehash: 44683b204ecd469f5f5412a7ec06e98ec8a4f37e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96224000"
---
# <a name="rangestart-function"></a><span data-ttu-id="c2605-102">Range Start-functie</span><span class="sxs-lookup"><span data-stu-id="c2605-102">RangeStart function</span></span>

<span data-ttu-id="c2605-103">Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="c2605-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="c2605-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c2605-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c2605-105">Retourneert de gedefinieerde begin waarde van het opgegeven bereik.</span><span class="sxs-lookup"><span data-stu-id="c2605-105">Returns the defined start value of the given range.</span></span>

```qsharp
function RangeStart (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="c2605-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c2605-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="c2605-107">bereik: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="c2605-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="c2605-108">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c2605-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c2605-109">De gedefinieerde begin waarde van het opgegeven bereik.</span><span class="sxs-lookup"><span data-stu-id="c2605-109">The defined start value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2605-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c2605-110">Remarks</span></span>

<span data-ttu-id="c2605-111">Het eerste element van een bereik expressie is `start` , het tweede element is, het `start+step` derde element `start+step+step` , enzovoort, totdat het `end` wordt door gegeven.</span><span class="sxs-lookup"><span data-stu-id="c2605-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="c2605-112">Houd er rekening mee dat de gedefinieerde begin waarde van een bereik hetzelfde is als het eerste element van de reeks, tenzij het bereik een lege reeks opgeeft (bijvoorbeeld 2..</span><span class="sxs-lookup"><span data-stu-id="c2605-112">Note that the defined start value of a range is the same as the first element of the sequence, unless the range specifies an empty sequence (for example, 2 ..</span></span> <span data-ttu-id="c2605-113">1).</span><span class="sxs-lookup"><span data-stu-id="c2605-113">1).</span></span>