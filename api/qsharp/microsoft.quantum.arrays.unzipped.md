---
uid: Microsoft.Quantum.Arrays.Unzipped
title: Uitgepakte functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unzipped
qsharp.summary: Given an array of 2-tuples, returns a tuple of two arrays, each containing the elements of the tuples of the input array.
ms.openlocfilehash: 7eea7982721dc596b8660be5f3634df71b1ddf95
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845369"
---
# <a name="unzipped-function"></a>Uitgepakte functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="example"></a>Voorbeeld

```qsharp
// split is same as ([6, 5, 5, 3, 2, 1], [true, false, false, false, true, false])
let split = Unzipped([(6, true), (5, false), (5, false), (3, false), (2, true), (1, false)]);
```

## <a name="see-also"></a>Zie ook

- [Microsoft.Quantum.Arrays.ZipPED](xref:Microsoft.Quantum.Arrays.Zipped)