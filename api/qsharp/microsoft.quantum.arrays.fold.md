---
uid: Microsoft.Quantum.Arrays.Fold
title: Functie vouwen
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: 47c23dd657391d80fe473d98f2036d8ddf1dbb0b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706004"
---
# <a name="fold-function"></a>Functie vouwen

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


Herhaalt een functie `f` via een matrix `array` , waarbij wordt geretourneerd `f(f(f(initialState, array[0]), array[1]), ...)` .

```qsharp
function Fold<'State, 'T> (folder : (('State, 'T) -> 'State), state : 'State, array : 'T[]) : 'State
```


## <a name="input"></a>Invoer

### <a name="folder--statet---state"></a>map: (status, niet)-> status

Een functie die over de matrix moet worden gevouwen.


### <a name="state--state"></a>status: ' State

De oorspronkelijke status van de map.


### <a name="array--t"></a>matrix: 'T []

Een matrix met waarden die moeten worden gevouwen.



## <a name="output--state"></a>Uitvoer: ' State

De uiteindelijke status die is geretourneerd door de map na het herhalen van alle elementen van `array` .

## <a name="type-parameters"></a>Type parameters

### <a name="state"></a>' Status

Het type statussen waarop de functie wordt uitgevoerd `folder` , dat wil zeggen, accepteert als eerste argument en retourneert.
### <a name="t"></a>T

Het type `array` elementen.