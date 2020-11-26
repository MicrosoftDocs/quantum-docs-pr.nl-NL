---
uid: Microsoft.Quantum.Arrays.Excluding
title: Functie uitsluiten
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Excluding
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: 6585e619834a96953c9eae2d36a8ebe0a11dbda0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221314"
---
# <a name="excluding-function"></a>Functie uitsluiten

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een matrix met de elementen van een andere matrix, met uitzonde ring van elementen in een bepaalde lijst met indices.

```qsharp
function Excluding<'T> (remove : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a>Invoer

### <a name="remove--int"></a>verwijderen: [int](xref:microsoft.quantum.lang-ref.int)[]

Een matrix met indices die aangeeft welke elementen moeten worden uitgesloten van de uitvoer.


### <a name="array--t"></a>matrix: 'T []

Matrix waarvan de waarden in de uitvoer matrix worden opgehaald.



## <a name="output--t"></a>Uitvoer: ' []

Een matrix `output` , bijvoorbeeld `output[0]` het eerste element van `array` waarvan de index niet wordt weer gegeven `remove` , zoals `output[1]` de tweede elementen, enzovoort.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van de matrix elementen.