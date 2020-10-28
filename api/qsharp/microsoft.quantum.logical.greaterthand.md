---
uid: Microsoft.Quantum.Logical.GreaterThanD
title: De functie GreaterThanD
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanD
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 20414e80e08993a18331a8f0b385a1e4cc1255b3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701481"
---
# <a name="greaterthand-function"></a>De functie GreaterThanD

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket [](https://nuget.org/packages/)


Retourneert waar als en alleen als een getal groter is dan een ander getal.

```qsharp
function GreaterThanD (a : Double, b : Double) : Bool
```


## <a name="input"></a>Invoer

### <a name="a--double"></a>a: [dubbel](xref:microsoft.quantum.lang-ref.double)

De eerste waarde die moet worden vergeleken.


### <a name="b--double"></a>b: [dubbel](xref:microsoft.quantum.lang-ref.double)

De tweede waarde die moet worden vergeleken.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` Als en alleen als dit `a` strikt groter is dan `b` .

## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```Q#
let cond = a > b;
let cond = GreaterThanD(a, b);
```