---
uid: Microsoft.Quantum.Arrays.Sorted
title: Functie gesorteerd
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Sorted
qsharp.summary: Given an array, returns the elements of that array sorted by a given comparison function.
ms.openlocfilehash: bd8b869e03c7f4687c456a944e07a811ae0d2ce2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220226"
---
# <a name="sorted-function"></a>Functie gesorteerd

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een matrix retourneert de elementen van die matrix, gesorteerd op een bepaalde vergelijkings functie.

```qsharp
function Sorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a>Invoer

### <a name="comparison--tt---bool"></a>vergelijking: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)

Een functie die twee elementen vergelijkt, zodat deze `a` kleiner is dan of gelijk is aan `b` if `comparison(a, b)` `true` .


### <a name="array--t"></a>matrix: 'T []

De matrix die moet worden gesorteerd.



## <a name="output--t"></a>Uitvoer: ' []



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van elk element van `array` .

## <a name="remarks"></a>Opmerkingen

Er `comparison` wordt van uitgegaan dat de functie transitief is, bijvoorbeeld als `comparison(a, b)` en `comparison(b, c)` `comparison(a, c)` wordt aangenomen. Als deze eigenschap niet in de wachtrij staat, is de uitvoer van deze functie mogelijk onjuist.

Aangezien dit een functie is, zijn de resultaten volledig determinstic, zelfs wanneer twee elementen worden beschouwd als gelijk onder `comparison` ; dat wil zeggen, wanneer `comparison(a, b)` en `comparison(b, a)` beide `true` .
Met name de sorteer bewerking die door deze functie wordt uitgevoerd, is gegarandeerd stabiel, zodat er twee elementen `a` `b` in die volg orde worden `array` weer gegeven en worden beschouwd als gelijk onder `comparison` `a` . deze worden ook voor `b` in de uitvoer opgenomen.

Bijvoorbeeld:

```Q#
function LastDigitLessThanOrEqual(left : Int, right : Int) : Bool {
    return LessThanOrEqualI(
        left % 10, right % 10
    );
}

function SortedByLastDigit() : Int[] {
    return Sorted(LastDigitLessThanOrEqual, [3, 37, 11, 17]);
}
// returns [11, 3, 37, 17].
```