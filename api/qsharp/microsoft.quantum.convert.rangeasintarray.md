---
uid: Microsoft.Quantum.Convert.RangeAsIntArray
title: De functie RangeAsIntArray
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Convert
qsharp.name: RangeAsIntArray
qsharp.summary: Creates an array `arr` of integers enumerated by start..step..end.
ms.openlocfilehash: 8c6b83d78e3b22ea1a17a48de66592950bf905a3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850104"
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

## <a name="example"></a>Voorbeeld

```qsharp
// The following returns [1,3,5,7];
let array = RangeAsIntArray(1..2..8);
```