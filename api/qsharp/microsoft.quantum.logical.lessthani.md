---
uid: Microsoft.Quantum.Logical.LessThanI
title: De functie LessThanI
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: LessThanI
qsharp.summary: Returns true if and only if a number is less than another number.
ms.openlocfilehash: 204e62a87d2b3d0070946985030d038ead686457
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708430"
---
# <a name="lessthani-function"></a>De functie LessThanI

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket [](https://nuget.org/packages/)


Retourneert waar als en alleen als een getal kleiner is dan een ander getal.

```qsharp
function LessThanI (a : Int, b : Int) : Bool
```


## <a name="input"></a>Invoer

### <a name="a--int"></a>a: [int](xref:microsoft.quantum.lang-ref.int)

De eerste waarde die moet worden vergeleken.


### <a name="b--int"></a>b: [int](xref:microsoft.quantum.lang-ref.int)

De tweede waarde die moet worden vergeleken.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` Als en alleen als dit `a` strikt kleiner is dan `b` .

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```Q#
let cond = a < b;
let cond = LessThanI(a, b);
```