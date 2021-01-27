---
uid: Microsoft.Quantum.Core.RangeStep
title: De functie RangeStep
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStep
qsharp.summary: Returns the integer that specifies how the next value of a range is calculated.
ms.openlocfilehash: 667b579337eec28d6b75de61668bd79de176883e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853602"
---
# <a name="rangestep-function"></a><span data-ttu-id="40970-102">De functie RangeStep</span><span class="sxs-lookup"><span data-stu-id="40970-102">RangeStep function</span></span>

<span data-ttu-id="40970-103">Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="40970-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="40970-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="40970-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="40970-105">Retourneert het gehele getal dat aangeeft hoe de volgende waarde van een bereik wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="40970-105">Returns the integer that specifies how the next value of a range is calculated.</span></span>

```qsharp
function RangeStep (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="40970-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="40970-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="40970-107">bereik: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="40970-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="40970-108">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="40970-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="40970-109">De gedefinieerde stap waarde van het opgegeven bereik.</span><span class="sxs-lookup"><span data-stu-id="40970-109">The defined step value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="40970-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="40970-110">Remarks</span></span>

<span data-ttu-id="40970-111">Het eerste element van een bereik expressie is `start` , het tweede element is, het `start+step` derde element `start+step+step` , enzovoort, totdat het `end` wordt door gegeven.</span><span class="sxs-lookup"><span data-stu-id="40970-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>