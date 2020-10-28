---
uid: Microsoft.Quantum.Core.RangeStart
title: Range Start-functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStart
qsharp.summary: Returns the defined start value of the given range.
ms.openlocfilehash: 3e4b0cebe34b4c98cb1d582a9cd11b46ff778517
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702837"
---
# <a name="rangestart-function"></a><span data-ttu-id="d4858-102">Range Start-functie</span><span class="sxs-lookup"><span data-stu-id="d4858-102">RangeStart function</span></span>

<span data-ttu-id="d4858-103">Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="d4858-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="d4858-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d4858-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d4858-105">Retourneert de gedefinieerde begin waarde van het opgegeven bereik.</span><span class="sxs-lookup"><span data-stu-id="d4858-105">Returns the defined start value of the given range.</span></span>

```qsharp
function RangeStart (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="d4858-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d4858-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="d4858-107">bereik: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="d4858-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="d4858-108">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d4858-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d4858-109">De gedefinieerde begin waarde van het opgegeven bereik.</span><span class="sxs-lookup"><span data-stu-id="d4858-109">The defined start value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="d4858-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d4858-110">Remarks</span></span>

<span data-ttu-id="d4858-111">Het eerste element van een bereik expressie is `start` , het tweede element is, het `start+step` derde element `start+step+step` , enzovoort, totdat het `end` wordt door gegeven.</span><span class="sxs-lookup"><span data-stu-id="d4858-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="d4858-112">Houd er rekening mee dat de gedefinieerde begin waarde van een bereik hetzelfde is als het eerste element van de reeks, tenzij het bereik een lege reeks opgeeft (bijvoorbeeld 2..</span><span class="sxs-lookup"><span data-stu-id="d4858-112">Note that the defined start value of a range is the same as the first element of the sequence, unless the range specifies an empty sequence (for example, 2 ..</span></span> <span data-ttu-id="d4858-113">1).</span><span class="sxs-lookup"><span data-stu-id="d4858-113">1).</span></span>