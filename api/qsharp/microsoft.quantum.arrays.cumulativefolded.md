---
uid: Microsoft.Quantum.Arrays.CumulativeFolded
title: De functie CumulativeFolded
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: CumulativeFolded
qsharp.summary: Combines Mapped and Fold into a single function
ms.openlocfilehash: 95cd5233a09a1234bba4de9fe870b9d93c0f86a4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846227"
---
# <a name="cumulativefolded-function"></a>De functie CumulativeFolded

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Combineert toegewezen en vouwen in één functie

```qsharp
function CumulativeFolded<'State, 'T> (fn : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State[]
```


## <a name="description"></a>Beschrijving

Met deze functie wordt de `fn` functie herhaald via de matrix, beginnend bij een begin status `state` en worden alle tussenliggende waarden geretourneerd, met inbegrip van de begin status.

## <a name="input"></a>Invoer

### <a name="fn--statet---state"></a>FN: (' State, 'T)-> '

Een functie die in de matrix moet worden gevouwen


### <a name="state--state"></a>status: ' State

De begin status die moet worden gevouwen


### <a name="array--t"></a>matrix: 'T []

Een matrix met waarden die moeten worden gevouwen



## <a name="output--state"></a>Uitvoer: ' status []

Alle tussenliggende statussen, inclusief de eind status, maar niet de begin status.
De lengte van de uitvoer matrix heeft dezelfde lengte als `array` .

## <a name="type-parameters"></a>Type parameters

### <a name="state"></a>' Status

Het type statussen waarop de `fn` functie wordt uitgevoerd, dat wil zeggen, accepteert als eerste invoer en retourneert.
### <a name="t"></a>T

Het type `array` elementen.

## <a name="example"></a>Voorbeeld

```qsharp
// same as sums = [1, 3, 6, 10, 15]
let sums = CumulativeFolded(PlusI, 0, SequenceI(1, 5));
```