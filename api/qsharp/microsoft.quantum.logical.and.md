---
uid: Microsoft.Quantum.Logical.And
title: En-functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: And
qsharp.summary: Returns the Boolean conjunction of two values.
ms.openlocfilehash: 6c405bdb4182cc7f32bd04952dec25a974c03445
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849231"
---
# <a name="and-function"></a>En-functie

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

```qsharp
let x = a and b;
let x = And(a, b);
```