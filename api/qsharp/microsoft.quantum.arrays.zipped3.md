---
uid: Microsoft.Quantum.Arrays.Zipped3
title: De functie Zipped3
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zipped3
qsharp.summary: Given three arrays, returns a new array of 3-tuples such that each 3-tuple contains an element from each original array.
ms.openlocfilehash: 6a4ffaeff8e6248a708ab9f8f9a6ff0c2e9e08d1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842180"
---
# <a name="zipped3-function"></a>De functie Zipped3

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Als er drie matrices zijn opgegeven, wordt een nieuwe matrix van 3-Tuples geretourneerd, zodat elke 3-tuple een element uit elke oorspronkelijke matrix bevat.

```qsharp
function Zipped3<'T1, 'T2, 'T3> (first : 'T1[], second : 'T2[], third : 'T3[]) : ('T1, 'T2, 'T3)[]
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

- [Microsoft.Quantum.Arrays.ZipPED](xref:Microsoft.Quantum.Arrays.Zipped)
- [Microsoft.Quantum.Arrays.Zipped4](xref:Microsoft.Quantum.Arrays.Zipped4)