---
uid: Microsoft.Quantum.Bitwise.LeftShiftedL
title: De functie LeftShiftedL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Bitwise
qsharp.name: LeftShiftedL
qsharp.summary: Shifts the bitwise representation of a number left by a given number of bits.
ms.openlocfilehash: 014653011574d0fabb4b9aa04cedf58b87ddf798
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842143"
---
# <a name="leftshiftedl-function"></a>De functie LeftShiftedL

Naam ruimte: [micro soft. Quantum. bitsgewijze](xref:Microsoft.Quantum.Bitwise)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt de bitsgewijze weer gave van een getal overgelaten door een bepaald aantal bits.

```qsharp
function LeftShiftedL (value : BigInt, amount : Int) : BigInt
```


## <a name="input"></a>Invoer

### <a name="value--bigint"></a>waarde: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

Het getal waarvan de bitsgewijze weer gave naar links moet worden verplaatst (significanter).


### <a name="amount--int"></a>bedrag: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal bits dat `value` naar links moet worden verplaatst.



## <a name="output--bigint"></a>Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

De waarde van `value` , naar links geschoven op `amount` bits.

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```qsharp
let c = a <<< b;
let c = LeftShiftedL(a, b);
```