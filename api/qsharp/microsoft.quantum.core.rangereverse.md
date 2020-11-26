---
uid: Microsoft.Quantum.Core.RangeReverse
title: De functie RangeReverse
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: 7bd7c55abe0b56b9d30b4c6e91f7175101dd2948
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213834"
---
# <a name="rangereverse-function"></a>De functie RangeReverse

Naam ruimte: [micro soft. Quantum. core](xref:Microsoft.Quantum.Core)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


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