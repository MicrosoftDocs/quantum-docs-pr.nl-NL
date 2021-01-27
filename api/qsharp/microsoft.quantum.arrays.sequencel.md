---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Sequence-functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 7e3c5c31428f9be152e28afbe478a3d15eb0a56c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850991"
---
# <a name="sequencel-function"></a>Sequence-functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Een matrix van gehele getallen ophalen binnen een bepaalde interval.

```qsharp
function SequenceL (from : BigInt, to : BigInt) : BigInt[]
```


## <a name="input"></a>Invoer

### <a name="from--bigint"></a>van: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

Een inclusieve start index van het interval.


### <a name="to--bigint"></a>naar: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

Een inclusieve eind index van het interval dat niet kleiner is dan `from` .



## <a name="output--bigint"></a>Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]

Een matrix met de volg orde van getallen `from` , `from + 1` ,..., `to` .

## <a name="example"></a>Voorbeeld

```qsharp
let arr1 = SequenceL(0L, 3L); // [0L, 1L, 2L, 3L]
let arr2 = SequenceL(23L, 29L); // [23L, 24L, 25L, 26L, 27L, 28L, 29L]
let arr3 = SequenceL(-5L, -2L); // [-5L, -4L, -3L, -2L]
```

## <a name="remarks"></a>Opmerkingen

Het verschil tussen `from` en `to` moet in een `Int` waarde passen.