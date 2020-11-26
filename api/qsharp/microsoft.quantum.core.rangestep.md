---
uid: Microsoft.Quantum.Core.RangeStep
title: De functie RangeStep
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeStep
qsharp.summary: Returns the integer that specifies how the next value of a range is calculated.
ms.openlocfilehash: 39c8581fe795a1b76d2a6e81c238a271287c2c38
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213800"
---
# <a name="rangestep-function"></a><span data-ttu-id="b67ff-102">De functie RangeStep</span><span class="sxs-lookup"><span data-stu-id="b67ff-102">RangeStep function</span></span>

<span data-ttu-id="b67ff-103">Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)</span><span class="sxs-lookup"><span data-stu-id="b67ff-103">Namespace: [Microsoft.Quantum.Core](xref:Microsoft.Quantum.Core)</span></span>

<span data-ttu-id="b67ff-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="b67ff-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="b67ff-105">Retourneert het gehele getal dat aangeeft hoe de volgende waarde van een bereik wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="b67ff-105">Returns the integer that specifies how the next value of a range is calculated.</span></span>

```qsharp
function RangeStep (range : Range) : Int
```


## <a name="input"></a><span data-ttu-id="b67ff-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b67ff-106">Input</span></span>

### <a name="range--range"></a><span data-ttu-id="b67ff-107">bereik: [bereik](xref:microsoft.quantum.lang-ref.range)</span><span class="sxs-lookup"><span data-stu-id="b67ff-107">range : [Range](xref:microsoft.quantum.lang-ref.range)</span></span>





## <a name="output--int"></a><span data-ttu-id="b67ff-108">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b67ff-108">Output : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b67ff-109">De gedefinieerde stap waarde van het opgegeven bereik.</span><span class="sxs-lookup"><span data-stu-id="b67ff-109">The defined step value of the given range.</span></span>

## <a name="remarks"></a><span data-ttu-id="b67ff-110">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="b67ff-110">Remarks</span></span>

<span data-ttu-id="b67ff-111">Het eerste element van een bereik expressie is `start` , het tweede element is, het `start+step` derde element `start+step+step` , enzovoort, totdat het `end` wordt door gegeven.</span><span class="sxs-lookup"><span data-stu-id="b67ff-111">A range expression's first element is `start`, its second element is `start+step`, third element is `start+step+step`, etc., until `end` is passed.</span></span>