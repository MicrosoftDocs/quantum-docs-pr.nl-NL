---
uid: Microsoft.Quantum.Logical.Conditioned
title: Voorwaarde functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: c0f55d4db95ad1f0d2b7f291cbc6ba8ae704cb81
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96198483"
---
# <a name="conditioned-function"></a>Voorwaarde functie

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een van twee waarden, afhankelijk van de waarde van een Booleaanse voor waarde.

```qsharp
function Conditioned<'T> (condition : Bool, ifTrue : 'T, ifFalse : 'T) : 'T
```


## <a name="input"></a>Invoer

### <a name="condition--bool"></a>voor waarde: [BOOL](xref:microsoft.quantum.lang-ref.bool)

Een voor waarde die wordt gebruikt om te bepalen welke invoer wordt geretourneerd.


### <a name="iftrue--t"></a>ifTrue: 'T

De waarde die moet worden geretourneerd `condition` Wanneer `true` .


### <a name="iffalse--t"></a>ifFalse: 'T

De waarde die moet worden geretourneerd `condition` Wanneer `false` .



## <a name="output--t"></a>Uitvoer: 'T

`ifTrue` Als dat zo `condition` is `true` , en `ifFalse` anders.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T



## <a name="remarks"></a>Opmerkingen

In tegens telling tot de `?|` operator is deze functie niet korte circuits, zodat beide invoer volledig worden geëvalueerd.

Tot het korte circuit, zijn de volgende equivalenten:

```Q#
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```