---
uid: Microsoft.Quantum.Arrays.Zip3
title: De functie Zip3
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip3
qsharp.summary: >-
  > [!WARNING]

  > Zip3 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped3> instead.


  Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: a6e7519755c4d473f6ba255ac5f877b2a3894d71
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219818"
---
# <a name="zip3-function"></a>De functie Zip3

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


> [!WARNING]
> Zip3 is afgeschaft. Gebruik <xref:Microsoft.Quantum.Arrays.Zipped3> in plaats daarvan.

Als er drie matrices zijn opgegeven, wordt een nieuwe matrix van 3-Tuples geretourneerd, zodat elke 3-tuple een element uit elke oorspronkelijke matrix bevat.

```qsharp
function Zip3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
```


## <a name="input"></a>Invoer

### <a name="first--t1"></a>eerst: 'T 1 []

Een matrix met waarden voor het eerste element van elke tuple.


### <a name="second--t2"></a>seconde: 'T 2 []

Een matrix met waarden voor het tweede element van elke tupel.


### <a name="third--t3"></a>derde: 'T 3 []

Een matrix met waarden voor het derde element van elke tupel.



## <a name="output--t1t2t3"></a>Uitvoer: (niet 1, niet 2, niet 3) []

Een matrix met drie Tuples van het formulier `(first[idx], second[idx], third[idx])` voor elke `idx` . Als de drie matrices een lengte hebben die niet even groot is, is de uitvoer zo lang als de kortste van de invoer.

## <a name="type-parameters"></a>Type parameters

### <a name="t1"></a>Niet 1

Het type van de eerste matrix elementen.
### <a name="t2"></a>Niet 2

Het type van de tweede matrix elementen.
### <a name="t3"></a>Niet 3

Het type van de derde matrix elementen.

## <a name="see-also"></a>Zie ook

- [Microsoft.Quantum.Arrays.Zip](xref:Microsoft.Quantum.Arrays.Zip)
- [Microsoft.Quantum.Arrays.Zip4](xref:Microsoft.Quantum.Arrays.Zip4)