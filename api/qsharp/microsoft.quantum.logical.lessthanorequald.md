---
uid: Microsoft.Quantum.Logical.LessThanOrEqualD
title: De functie LessThanOrEqualD
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanOrEqualD
qsharp.summary: Returns true if and only if a number is less than or equal to another number.
ms.openlocfilehash: 7b0e9da379bd67eb78a80e7a535a15dcb8ba85c7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701457"
---
# <a name="lessthanorequald-function"></a>De functie LessThanOrEqualD

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket [](https://nuget.org/packages/)


Retourneert waar als en alleen als een getal kleiner is dan of gelijk is aan een ander getal.

```qsharp
function LessThanOrEqualD (a : Double, b : Double) : Bool
```


## <a name="input"></a>Invoer

### <a name="a--double"></a>a: [dubbel](xref:microsoft.quantum.lang-ref.double)

De eerste waarde die moet worden vergeleken.


### <a name="b--double"></a>b: [dubbel](xref:microsoft.quantum.lang-ref.double)

De tweede waarde die moet worden vergeleken.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` Als en alleen als deze `a` kleiner is dan of gelijk is aan `b` .

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```Q#
let cond = a <= b;
let cond = LessThanOrEqualD(a, b);
```