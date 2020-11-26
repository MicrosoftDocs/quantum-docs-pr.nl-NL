---
uid: Microsoft.Quantum.Arrays.Zipped4
title: De functie Zipped4
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped4
qsharp.summary: Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: d5ee10ac9776383e75bc16a5c003a8b1a65c5698
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219631"
---
# <a name="zipped4-function"></a>De functie Zipped4

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Gegeven vier matrices retourneert een nieuwe matrix van 4 Tuples, zodat elke 4-tuple een element uit elke oorspronkelijke matrix bevat.

```qsharp
function Zipped4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
```


## <a name="input"></a>Invoer

### <a name="first--t1"></a>eerst: 'T 1 []

Een matrix met waarden voor het eerste element van elke tuple.


### <a name="second--t2"></a>seconde: 'T 2 []

Een matrix met waarden voor het tweede element van elke tupel.


### <a name="third--t3"></a>derde: 'T 3 []

Een matrix met waarden voor het derde element van elke tupel.


### <a name="fourth--t4"></a>vierde: 'T 4 []

Een matrix met waarden voor het vierde element van elke tupel.



## <a name="output--t1t2t3t4"></a>Uitvoer: (niet 1, 'T 2, niet 3, niet 4) []

Een matrix met vier Tuples van het formulier `(first[idx], second[idx], third[idx], fourth[idx])` voor elke `idx` . Als de vier matrices een lengte hebben die niet even groot is, is de uitvoer zo lang als de kortste van de invoer.

## <a name="type-parameters"></a>Type parameters

### <a name="t1"></a>Niet 1

Het type van de eerste matrix elementen.
### <a name="t2"></a>Niet 2

Het type van de tweede matrix elementen.
### <a name="t3"></a>Niet 3

Het type van de derde matrix elementen.
### <a name="t4"></a>Niet 4

Het type van de vierde matrix elementen.

## <a name="see-also"></a>Zie ook

- [Microsoft.Quantum.Arrays.ZipPED](xref:Microsoft.Quantum.Arrays.Zipped)
- [Microsoft.Quantum.Arrays.ZipPED3](xref:Microsoft.Quantum.Arrays.Zipped3)