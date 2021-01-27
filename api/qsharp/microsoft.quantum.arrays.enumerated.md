---
uid: Microsoft.Quantum.Arrays.Enumerated
title: Opgesomde functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Enumerated
qsharp.summary: Given an array, returns a new array containing elements of the original array along with the indices of each element.
ms.openlocfilehash: adb13d8b25c9e4a6011ade119ffa3cb2783f60e2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848131"
---
# <a name="enumerated-function"></a>Opgesomde functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een matrix retourneert een nieuwe matrix met elementen van de oorspronkelijke matrix, samen met de indices van elk element.

```qsharp
function Enumerated<'TElement> (array : 'TElement[]) : (Int, 'TElement)[]
```


## <a name="input"></a>Invoer

### <a name="array--telement"></a>matrix: ' TEle []

Een matrix waarvan de elementen moeten worden geïnventariseerd.



## <a name="output--inttelement"></a>Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int), ' tele) []

Een nieuwe matrix met elementen van de oorspronkelijke matrix samen met de indices.

## <a name="type-parameters"></a>Type parameters

### <a name="telement"></a>-TEle

Het type elementen van de matrix.

## <a name="example"></a>Voorbeeld

De volgende `for` lussen zijn gelijk:

```qsharp
for (idx in IndexRange(array)) {
    let element = array[idx];
    ...
}
for ((idx, element) in Enumerated(array)) { ... }
```