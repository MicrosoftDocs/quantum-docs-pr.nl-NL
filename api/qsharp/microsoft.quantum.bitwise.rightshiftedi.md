---
uid: Microsoft.Quantum.Bitwise.RightShiftedI
title: De functie RightShiftedI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedI
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: b20a4a8c281a470af9a4828f8a5ca905a7918723
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209771"
---
# <a name="rightshiftedi-function"></a>De functie RightShiftedI

Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt de bitsgewijze weer gave van een getal naar rechts verplaatst met een opgegeven aantal bits.

```qsharp
function RightShiftedI (value : Int, amount : Int) : Int
```


## <a name="input"></a>Invoer

### <a name="value--int"></a>waarde: [int](xref:microsoft.quantum.lang-ref.int)

Het getal waarvan de bitsgewijze weer gave naar rechts wordt geschoven (minder significant).


### <a name="amount--int"></a>bedrag: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal bits dat `value` naar rechts wordt geschoven.



## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

De waarde van `value` , naar geschoven op `amount` bits.

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```Q#
let c = a >>> b;
let c = RightShiftedI(a, b);
```