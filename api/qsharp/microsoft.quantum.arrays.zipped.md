---
uid: Microsoft.Quantum.Arrays.Zipped
title: Gezipte functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped
qsharp.summary: Given two arrays, returns a new array of pairs such that each pair contains an element from each original array.
ms.openlocfilehash: 67170fa005675f0e5d788c9c3b350fb9a961a597
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705669"
---
# <a name="zipped-function"></a>Gezipte functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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

## <a name="see-also"></a>Zie ook

- [Microsoft.Quantum.Arrays.ZipPED3](xref:Microsoft.Quantum.Arrays.Zipped3)
- [Microsoft.Quantum.Arrays.Zipped4](xref:Microsoft.Quantum.Arrays.Zipped4)
- [Micro soft. Quantum. arrays. ungezipte](xref:Microsoft.Quantum.Arrays.Unzipped)