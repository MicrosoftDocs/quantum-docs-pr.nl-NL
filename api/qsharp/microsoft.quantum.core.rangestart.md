---
uid: Microsoft.Quantum.Core.RangeStart
title: Range Start-functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStart
qsharp.summary: Returns the defined start value of the given range.
ms.openlocfilehash: 5b04e8c860a4bd6af7b10b4dbf803b1eb69ef5d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98831121"
---
# <a name="rangestart-function"></a><span data-ttu-id="d6b34-102">Range Start-functie</span><span class="sxs-lookup"><span data-stu-id="d6b34-102">RangeStart function</span></span>

<span data-ttu-id="d6b34-103">Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="d6b34-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="d6b34-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="d6b34-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="d6b34-105">Retourneert de gedefinieerde begin waarde van het opgegeven bereik.</span><span class="sxs-lookup"><span data-stu-id="d6b34-105">Returns the defined start value of the given range.</span></span>

```qsharp
function RangeStart (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="d6b34-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d6b34-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="d6b34-107">bereik: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="d6b34-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="d6b34-108">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d6b34-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d6b34-109">De gedefinieerde begin waarde van het opgegeven bereik.</span><span class="sxs-lookup"><span data-stu-id="d6b34-109">The defined start value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6b34-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d6b34-110">Remarks</span></span>

<span data-ttu-id="d6b34-111">Het eerste element van een bereik expressie is `start` , het tweede element is, het `start+step` derde element `start+step+step` , enzovoort, totdat het `end` wordt door gegeven.</span><span class="sxs-lookup"><span data-stu-id="d6b34-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>

<span data-ttu-id="d6b34-112">Houd er rekening mee dat de gedefinieerde begin waarde van een bereik hetzelfde is als het eerste element van de reeks, tenzij het bereik een lege reeks opgeeft (bijvoorbeeld 2..</span><span class="sxs-lookup"><span data-stu-id="d6b34-112">Note that the defined start value of a range is the same as the first element of the sequence, unless the range specifies an empty sequence (for example, 2 ..</span></span> <span data-ttu-id="d6b34-113">1).</span><span class="sxs-lookup"><span data-stu-id="d6b34-113">1).</span></span>