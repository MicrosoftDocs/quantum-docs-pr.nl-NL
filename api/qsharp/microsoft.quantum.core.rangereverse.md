---
uid: Microsoft.Quantum.Core.RangeReverse
title: De functie RangeReverse
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Core
qsharp.name: RangeReverse
qsharp.summary: Returns a new range which is the reverse of the input range.
ms.openlocfilehash: f3b94d3c6fa6350a2c337f8bc8d889d24d87a85b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853646"
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