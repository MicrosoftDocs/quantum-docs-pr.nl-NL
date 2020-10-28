---
uid: Microsoft.Quantum.Logical.Conditioned
title: Voorwaarde functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: 8aabe8b018129ddee3b934c207d0a62e59fb6f4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707053"
---
# <a name="conditioned-function"></a>Voorwaarde functie

Naam ruimte: [micro soft. Quantum. Logical](xref:Microsoft.Quantum.Logical)

Pakket [](https://nuget.org/packages/)


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