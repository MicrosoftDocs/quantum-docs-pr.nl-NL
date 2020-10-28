---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: De functie RangeAsIntArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: bd3ac51d2925d7a4450b2bc5e6f7899fcab18f2c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702921"
---
# <a name="rangeasintarray-function"></a>De functie RangeAsIntArray

Naam ruimte: [micro soft. Quantum. Convert](xref:Microsoft.Quantum.Convert)

Pakket [](https://nuget.org/packages/)


Maakt een matrix `arr` met gehele getallen die worden opgesomd door start.. stap.. endsystemen.

```qsharp
function RangeAsIntArray (range : Range) : Int[]
```


## <a name="input"></a>Invoer

### <a name="range--range"></a>bereik: [bereik](xref:microsoft.quantum.lang-ref.range)

Een `Range` van de waarden `start..step..end` die moeten worden geconverteerd naar een matrix.



## <a name="output--int"></a>Output: [int](xref:microsoft.quantum.lang-ref.int)[]

Een nieuwe matrix van gehele getallen die overeenkomen met waarden die worden herhaald door `range` .