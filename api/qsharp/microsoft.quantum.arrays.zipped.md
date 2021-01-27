---
uid: Microsoft.Quantum.Arrays.Zipped
title: Gezipte functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped
qsharp.summary: Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 5177ab0ade5a9ad7788e60c1028befb84b0191d4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845335"
---
# <a name="zipped-function"></a>Gezipte functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Als er twee matrices worden opgegeven, wordt er een nieuwe matrix van paren geretourneerd, zodat elk paar een element uit elke oorspronkelijke matrix bevat.

```qsharp
function Zipped<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
```


## <a name="input"></a>Invoer

### <a name="left--t"></a>links: ' []

Een matrix met waarden voor het eerste element van elke tuple.


### <a name="right--u"></a>rechts: ' U []

Een matrix met waarden voor het tweede element van elke tupel.



## <a name="output--tu"></a>Uitvoer: ('T, ' U) []

Een matrix die de paren van het formulier bevat `(left[idx], right[idx])` `idx` . Als de twee matrices een lengte hebben die niet even groot is, is de uitvoer zo lang als de kortste van de invoer.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van de elementen van de linker matrix.
### <a name="u"></a>' U

Het type van de rechter matrix elementen.

## <a name="example"></a>Voorbeeld

```qsharp
let left = [1, 3, 71];
let right = [false, true];
let pairs = Zipped(left, right); // [(1, false), (3, true)]
```

## <a name="see-also"></a>Zie ook

- [Microsoft.Quantum.Arrays.ZipPED3](xref:Microsoft.Quantum.Arrays.Zipped3)
- [Microsoft.Quantum.Arrays.Zipped4](xref:Microsoft.Quantum.Arrays.Zipped4)
- [Micro soft. Quantum. arrays. ungezipte](xref:Microsoft.Quantum.Arrays.Unzipped)