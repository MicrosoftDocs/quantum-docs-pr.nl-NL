---
uid: Microsoft.Quantum.Logical.GreaterThanD
title: De functie GreaterThanD
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: GreaterThanD
qsharp.summary: Returns true if and only if a number is greater than another number.
ms.openlocfilehash: 26a963645758b6de83654304c38830af5c561b3a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849223"
---
# <a name="greaterthand-function"></a>De functie GreaterThanD

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

```qsharp
let cond = a > b;
let cond = GreaterThanD(a, b);
```