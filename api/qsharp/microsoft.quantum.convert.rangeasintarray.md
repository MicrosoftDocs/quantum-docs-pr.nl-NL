---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: De functie RangeAsIntArray
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: f756e42aef7dc600e1fc6943a02513ac791f2320
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214004"
---
# <a name="rangeasintarray-function"></a>De functie RangeAsIntArray

Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Maakt een matrix `arr` met gehele getallen die worden opgesomd door start.. stap.. endsystemen.

```qsharp
function RangeAsIntArray (range : Range) : Int[]
```


## <a name="input"></a>Invoer

### <a name="range--range"></a>bereik: [bereik](xref:microsoft.quantum.lang-ref.range)

Een `Range` van de waarden `start..step..end` die moeten worden geconverteerd naar een matrix.



## <a name="output--int"></a>Output: [int](xref:microsoft.quantum.lang-ref.int)[]

Een nieuwe matrix van gehele getallen die overeenkomen met waarden die worden herhaald door `range` .