---
uid: Microsoft.Quantum.Bitwise.RightShiftedL
title: De functie RightShiftedL
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedL
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 3d941e1a0bcd96fe54ab01019293d883f11547a1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219512"
---
# <a name="rightshiftedl-function"></a>De functie RightShiftedL

Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt de bitsgewijze weer gave van een getal naar rechts verplaatst met een opgegeven aantal bits.

```qsharp
function RightShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a>Invoer

### <a name="value--bigint"></a>waarde: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

Het getal waarvan de bitsgewijze weer gave naar rechts wordt geschoven (minder significant).


### <a name="amount--int"></a>bedrag: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal bits dat `value` naar rechts wordt geschoven.



## <a name="output--bigint"></a>Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

De waarde van `value` , naar geschoven op `amount` bits.

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```Q#
let c = a >>> b;
let c = RightShiftedL(a, b);
```