---
uid: Microsoft.Quantum.Arrays.Zip4
title: De functie Zip4
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Zip4
qsharp.summary: >-
  > [!WARNING]

  > Zip4 has been deprecated. Please use <xref:Microsoft.Quantum.Arrays.Zipped4> instead.


  Given four arrays, returns a new array of 4-tuples such that each 4-tuple contains an element from each original array.
ms.openlocfilehash: d42b3b6db059163f6c766d4f133551be293c153d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705661"
---
# <a name="zip4-function"></a>De functie Zip4

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


> [!WARNING]
> Zip4 is afgeschaft. Gebruik <xref:Microsoft.Quantum.Arrays.Zipped4> in plaats daarvan.

Gegeven vier matrices retourneert een nieuwe matrix van 4 Tuples, zodat elke 4-tuple een element uit elke oorspronkelijke matrix bevat.

```qsharp
function Zip4<'T1, 'T2, 'T3, 'T4> (first : 'T1[], second : 'T2[], third : 'T3[], fourth : 'T4[]) : ('T1, 'T2, 'T3, 'T4)[]
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

- [Microsoft.Quantum.Arrays.Zip](xref:Microsoft.Quantum.Arrays.Zip)
- [Microsoft.Quantum.Arrays.Zip3](xref:Microsoft.Quantum.Arrays.Zip3)