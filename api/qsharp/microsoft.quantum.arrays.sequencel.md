---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Sequence-functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 3e5c7f64825f09d82792d3e46fe3f53f5814510b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220260"
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

## <a name="remarks"></a>Opmerkingen

Het verschil tussen `from` en `to` moet in een `Int` waarde passen.