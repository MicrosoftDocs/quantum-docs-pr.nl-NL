---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Sequence-functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5ce63575e703341fce42c0be393765c342bbd89
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705781"
---
# <a name="sequencel-function"></a>Sequence-functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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