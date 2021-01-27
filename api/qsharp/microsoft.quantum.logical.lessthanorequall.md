---
uid: Microsoft.Quantum.Logical.LessThanOrEqualL
title: De functie LessThanOrEqualL
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualL
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 1de3fdb0fa53fef9cbf4b9ee9b6a1c54865bd093
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849121"
---
# <a name="lessthanorequall-function"></a>De functie LessThanOrEqualL

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert waar als en alleen als een getal kleiner is dan of gelijk is aan een ander getal.

```qsharp
function LessThanOrEqualL (a : BigInt, b : BigInt) : Bool
```


## <a name="input"></a>Invoer

### <a name="a--bigint"></a>a: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

De eerste waarde die moet worden vergeleken.


### <a name="b--bigint"></a>b: [BigInt](xref:microsoft.quantum.lang-ref.bigint)

De tweede waarde die moet worden vergeleken.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` Als en alleen als deze `a` kleiner is dan of gelijk is aan `b` .

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```qsharp
let cond = a <= b;
let cond = LessThanOrEqualL(a, b);
```