---
uid: Microsoft.Quantum.Arrays.Fold
title: Functie vouwen
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Fold
qsharp.summary: Iterates a function `f` through an array `array`, returning `f(f(f(initialState, array[0]), array[1]), ...)`.
ms.openlocfilehash: d12e070058178ce2cbdd70cade5bc16607a55d5e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848609"
---
# <a name="fold-function"></a>Functie vouwen

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="example"></a>Voorbeeld

```qsharp
function Plus(a : Double, b : Double) {
    return a + b;
}
function Sum(xs : Double[]) {
    return Fold(Plus, 0.0, xs);
}
```