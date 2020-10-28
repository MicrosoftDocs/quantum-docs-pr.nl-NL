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
# <a name="rangestep-function"></a>De functie RangeStep

Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)

Pakket [](https://nuget.org/packages/)


Retourneert het gehele getal dat aangeeft hoe de volgende waarde van een bereik wordt berekend.

```qsharp
function RangeStep (range : Range) : Int
```


## <a name="input"></a>Invoer

### <a name="range--range"></a>bereik: [bereik](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

De gedefinieerde stap waarde van het opgegeven bereik.

## <a name="remarks"></a>Opmerkingen

Het eerste element van een bereik expressie is `start` , het tweede element is, het `start+step` derde element `start+step+step` , enzovoort, totdat het `end` wordt door gegeven.