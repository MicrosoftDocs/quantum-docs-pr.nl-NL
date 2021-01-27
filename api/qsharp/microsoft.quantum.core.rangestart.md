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