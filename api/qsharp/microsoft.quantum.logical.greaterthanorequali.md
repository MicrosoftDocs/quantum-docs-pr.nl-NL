---
uid: Microsoft.Quantum.Logical.GreaterThanOrEqualI
title: De functie GreaterThanOrEqualI
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanOrEqualI
qsharp.summary: Returns true if and only if a number is greater than or equal to another number.
ms.openlocfilehash: c1a513500c8a70bd7628976974387cba48162e80
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849187"
---
# <a name="greaterthanorequali-function"></a>De functie GreaterThanOrEqualI

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert waar als en alleen als een getal groter is dan of gelijk is aan een ander getal.

```qsharp
function GreaterThanOrEqualI (a : Int, b : Int) : Bool
```


## <a name="input"></a>Invoer

### <a name="a--int"></a>a: [int](xref:microsoft.quantum.lang-ref.int)

De eerste waarde die moet worden vergeleken.


### <a name="b--int"></a>b: [int](xref:microsoft.quantum.lang-ref.int)

De tweede waarde die moet worden vergeleken.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` Als en alleen als dit `a` groter is dan of gelijk is aan `b` .

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```qsharp
let cond = a >= b;
let cond = GreaterThanOrEqualI(a, b);
```