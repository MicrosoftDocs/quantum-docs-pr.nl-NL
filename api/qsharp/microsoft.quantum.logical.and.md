---
uid: Microsoft.Quantum.Logical.And
title: En-functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: cc81f650216c4db219a79c4fe89a42447a4e95b8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707061"
---
# <a name="and-function"></a>En-functie

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket [](https://nuget.org/packages/)


Retourneert de Booleaanse combi natie van twee waarden.

```qsharp
function And (a : Bool, b : Bool) : Bool
```


## <a name="input"></a>Invoer

### <a name="a--bool"></a>a: [BOOL](xref:microsoft.quantum.lang-ref.bool)

De eerste waarde die moet worden overwogen.


### <a name="b--bool"></a>b: [BOOL](xref:microsoft.quantum.lang-ref.bool)

De tweede waarde die moet worden overwogen.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` Als en alleen als `a` en `b` beide `true` .

## <a name="remarks"></a>Opmerkingen

In tegens telling tot de `and` operator is deze functie niet korte circuits, zodat beide invoer volledig worden geëvalueerd.

Tot het korte circuit, zijn de volgende equivalenten:

```Q#
let x = a and b;
let x = And(a, b);
```