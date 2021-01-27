---
uid: Microsoft.Quantum.Bitwise.RightShiftedL
title: De functie RightShiftedL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: RightShiftedL
qsharp.summary: Shifts the bitwise representation of a number right by a given number of bits.
ms.openlocfilehash: 03ed69c7151e62b91c4a036e301f99b45ce5ab62
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842101"
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

```qsharp
let c = a >>> b;
let c = RightShiftedL(a, b);
```