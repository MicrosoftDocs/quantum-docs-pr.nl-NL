---
uid: Microsoft.Quantum.Arrays.Zip
title: Zip-functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip
qsharp.summary: >-
  > [!WARNING]

  > Zip has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped> instead.


  Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 44db8d38d96babd16ead5ae6dde91da23bdee2c9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219852"
---
# <a name="zip-function"></a>Zip-functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> Zip is afgeschaft. Gebruik <xref:Microsoft.Quantum.Arrays.Zipped> in plaats daarvan.

Als er twee matrices worden opgegeven, wordt er een nieuwe matrix van paren geretourneerd, zodat elk paar een element uit elke oorspronkelijke matrix bevat.

```qsharp
function Zip<'T, 'U> (left : 'T[], right : 'U[]) : ('T, 'U)[]
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

## <a name="see-also"></a>Zie ook

- [Microsoft.Quantum.Arrays.Zip3](xref:Microsoft.Quantum.Arrays.Zip3)
- [Microsoft.Quantum.Arrays.Zip4](xref:Microsoft.Quantum.Arrays.Zip4)
- [Micro soft. Quantum. arrays. ungezipte](xref:Microsoft.Quantum.Arrays.Unzipped)