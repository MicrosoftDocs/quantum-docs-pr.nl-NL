---
uid: Microsoft.Quantum.Arrays.IsSorted
title: De functie IsSorted
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsSorted
qsharp.summary: Given an array, returns whether that array is sorted as defined by a given comparison function.
ms.openlocfilehash: b2c5f11c0d92ddf9214de2d439c175319c569be0
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220828"
---
# <a name="issorted-function"></a>De functie IsSorted

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert aan de hand van een matrix of die matrix is gesorteerd zoals gedefinieerd door een bepaalde vergelijkings functie.

```qsharp
function IsSorted<'T> (comparison : (('T, 'T) -> Bool), array : 'T[]) : Bool
```


## <a name="input"></a>Invoer

### <a name="comparison--tt---bool"></a>vergelijking: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)

Een functie die twee elementen vergelijkt, zodat deze `a` kleiner is dan of gelijk is aan `b` if `comparison(a, b)` `true` .


### <a name="array--t"></a>matrix: 'T []

De matrix die moet worden gecontroleerd.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

`true` Als en alleen als voor elk paar elementen `a` en voor `b` `array` komen in die volg orde, `comparison(a, b)` is `true` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van elk element van `array` .

## <a name="remarks"></a>Opmerkingen

Er `comparison` wordt van uitgegaan dat de functie transitief is, bijvoorbeeld als `comparison(a, b)` en `comparison(b, c)` `comparison(a, c)` wordt aangenomen. Als deze eigenschap niet in de wachtrij staat, is de uitvoer van deze functie mogelijk onjuist.