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
# <a name="rangeend-function"></a>De functie RangeEnd

Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)

Pakket [](https://nuget.org/packages/)


Retourneert de gedefinieerde eind waarde van het opgegeven bereik. Dit is niet noodzakelijkerwijs het laatste element in de reeks.

```qsharp
function RangeEnd (range : Range) : Int
```


## <a name="input"></a>Invoer

### <a name="range--range"></a>bereik: [bereik](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

De gedefinieerde eind waarde van het opgegeven bereik.

## <a name="remarks"></a>Opmerkingen

Het eerste element van een bereik expressie is `start` , het tweede element is, het `start+step` derde element `start+step+step` , enzovoort, totdat het `end` wordt door gegeven.

Houd er rekening mee dat de gedefinieerde eind waarde van een bereik kan verschillen van het laatste element in de reeks die is opgegeven door het bereik. bijvoorbeeld in een bereik van 0.. 2.. 5 het laatste element is 4, maar de eind waarde is 5.