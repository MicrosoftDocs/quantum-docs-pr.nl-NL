---
uid: Microsoft.Quantum.Arrays.Exclude
title: De functie exclude
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Exclude
qsharp.summary: Returns an array containing the elements of another array, excluding elements at a given list of indices.
ms.openlocfilehash: e1fa7e728d4846db90872055454a8182a77a518b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706052"
---
# <a name="exclude-function"></a>De functie exclude

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


Retourneert een matrix met de elementen van een andere matrix, met uitzonde ring van elementen in een bepaalde lijst met indices.

```qsharp
function Exclude<'T> (remove : Int[], array : 'T[]) : 'T[]
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