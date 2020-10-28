---
uid: Microsoft.Quantum.Core.RangeReverse
title: De functie RangeReverse
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: d4e612d2f175015b7193634aeec12f9df12df7d3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702866"
---
# <a name="rangereverse-function"></a>De functie RangeReverse

Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)

Pakket [](https://nuget.org/packages/)


Retourneert een nieuw bereik dat het omgekeerde is van het invoer bereik.

```qsharp
function RangeReverse (r : Range) : Range
```


## <a name="input"></a>Invoer

### <a name="r--range"></a>r: [bereik](xref:microsoft.quantum.lang-ref.range)

Invoer bereik.



## <a name="output--range"></a>Uitvoer: [bereik](xref:microsoft.quantum.lang-ref.range)

Een nieuw bereik dat het omgekeerde is van het opgegeven bereik.

## <a name="remarks"></a>Opmerkingen

Houd er rekening mee dat het omgekeerde van een bereik niet gewoon `end` .. `-step` .. is `start` , omdat het daad werkelijke laatste element van een bereik mogelijk niet hetzelfde is als `end` .