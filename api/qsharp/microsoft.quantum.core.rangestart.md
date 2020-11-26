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
# <a name="rangestart-function"></a>Range Start-functie

Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retourneert de gedefinieerde begin waarde van het opgegeven bereik.

```qsharp
function RangeStart (range : Range) : Int
```


## <a name="input"></a>Invoer

### <a name="range--range"></a>bereik: [bereik](xref:microsoft.quantum.lang-ref.range)





## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

De gedefinieerde begin waarde van het opgegeven bereik.

## <a name="remarks"></a>Opmerkingen

Het eerste element van een bereik expressie is `start` , het tweede element is, het `start+step` derde element `start+step+step` , enzovoort, totdat het `end` wordt door gegeven.

Houd er rekening mee dat de gedefinieerde begin waarde van een bereik hetzelfde is als het eerste element van de reeks, tenzij het bereik een lege reeks opgeeft (bijvoorbeeld 2.. 1).