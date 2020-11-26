---
uid: Microsoft.Quantum.Bitwise.LeftShiftedI
title: De functie LeftShiftedI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedI
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 3a7220489bfa241e2337df14291bafb1d6e0e19e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209856"
---
# <a name="leftshiftedi-function"></a>De functie LeftShiftedI

Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt de bitsgewijze weer gave van een getal overgelaten door een bepaald aantal bits.

```qsharp
function LeftShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a>Invoer

### <a name="value--int"></a>waarde: [int](xref:microsoft.quantum.lang-ref.int)

Het getal waarvan de bitsgewijze weer gave naar links moet worden verplaatst (significanter).


### <a name="amount--int"></a>bedrag: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal bits dat `value` naar links moet worden verplaatst.



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

De waarde van `value` , naar links geschoven op `amount` bits.

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```Q#
let c = a <<< b;
let c = LeftShiftedI(a, b);
```