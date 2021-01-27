---
uid: Microsoft.Quantum.Logical.Conditioned
title: Voorwaarde functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Logical
qsharp.name: Conditioned
qsharp.summary: Returns one of two values, depending on the value of a Boolean condition.
ms.openlocfilehash: ea3b8eba960acceb6540978c6fccd9f796b0f67d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98817290"
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

```qsharp
let x = condition ? ifTrue | ifFalse;
let x = Conditioned(condition, ifTrue, ifFalse);
```