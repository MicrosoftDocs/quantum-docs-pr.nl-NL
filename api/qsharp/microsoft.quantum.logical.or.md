---
uid: Microsoft.Quantum.Logical.Or
title: Or-functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Or
qsharp.summary: Returns the Boolean disjunction of two values.
ms.openlocfilehash: 98a416229386461b241d087b7ae95f078f8be70a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706516"
---
# <a name="or-function"></a>Or-functie

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket [](https://nuget.org/packages/)


Retourneert de Booleaanse schei ding van twee waarden.

```qsharp
function Or (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>Invoer

### <a name="a--bool"></a>a: [BOOL](xref:microsoft.quantum.lang-ref.bool)

De eerste waarde die moet worden overwogen.


### <a name="b--bool"></a>b: [BOOL](xref:microsoft.quantum.lang-ref.bool)

De tweede waarde die moet worden overwogen.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` Als en alleen als dat wel of het geval `a` `b` is `true` .

## <a name="remarks"></a>Opmerkingen

In tegens telling tot de `or` operator is deze functie niet korte circuits, zodat beide invoer volledig worden geëvalueerd.

Tot het korte circuit, zijn de volgende equivalenten:

```Q#
let x = a or b;
let x = Or(a, b);
```