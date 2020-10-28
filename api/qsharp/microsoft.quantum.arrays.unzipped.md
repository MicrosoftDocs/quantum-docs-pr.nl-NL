---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Uitgepakte functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: 37c960dc5dbdb8099fbebe1ad63cb44ce642733c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705724"
---
# <a name="unzipped-function"></a>Uitgepakte functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


Op basis van een matrix van 2-Tuples retourneert een tuple van twee matrices, elk met de elementen van de Tuples van de invoer matrix.

```qsharp
function Unzipped<'T, 'U> (arr : ('T, 'U)[]) : ('T[], 'U[])
```


## <a name="input"></a>Invoer

### <a name="arr--tu"></a>ARR: ('T, ' U) []

Een matrix met 2-Tuples



## <a name="output--tu"></a>Uitvoer: ('T [], ' U [])

Twee matrices, de eerste die alle eerste elementen van de ingevoerde Tuples bevat, de tweede matrix met alle tweede elementen van de ingevoerde Tuples.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van het eerste element in elke tupel
### <a name="u"></a>' U

Het type van het tweede element in elke tupel

## <a name="see-also"></a>Zie ook

- [Microsoft.Quantum.Arrays.ZipPED](xref:Microsoft.Quantum.Arrays.Zipped)