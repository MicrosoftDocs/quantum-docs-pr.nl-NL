---
uid: Microsoft.Quantum.Arrays.CumulativeFolded
title: De functie CumulativeFolded
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: CumulativeFolded
qsharp.summary: Combines Mapped and Fold into a single function
ms.openlocfilehash: a09c2779c8f06d8f6b7b0902366f3cefbbca4525
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706125"
---
# <a name="cumulativefolded-function"></a>De functie CumulativeFolded

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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