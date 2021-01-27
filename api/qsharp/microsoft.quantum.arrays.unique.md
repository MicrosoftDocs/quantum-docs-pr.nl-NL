---
uid: Microsoft.Quantum.Arrays.Unique
title: Unieke functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: b3aa03d20195bdd8bb64783a9b68cafac29e68f6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850911"
---
# <a name="unique-function"></a>Unieke functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een nieuwe matrix die geen gelijk aan aangrenzende elementen heeft.

```qsharp
function Unique<'T> (equal : (('T, 'T) -> Bool), array : 'T[]) : 'T[]
```


## <a name="description"></a>Beschrijving

Op basis van een aantal elementen en een functie om gelijkheid te testen, retourneert deze functie een nieuwe matrix waarin de relatieve volg orde van elementen wordt behouden, maar alle aangrenzende elementen die gelijk zijn, worden gefilterd op slechts één element.

## <a name="input"></a>Invoer

### <a name="equal--tt---bool"></a>gelijk aan: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)

Een functie waarmee twee elementen worden vergeleken, zoals die worden `a` beschouwd als gelijk aan `b` `equal(a, b)` `true` .


### <a name="array--t"></a>matrix: 'T []

De matrix die moet worden gefilterd op unieke elementen.



## <a name="output--t"></a>Uitvoer: ' []

Matrix zonder gelijke aangrenzende elementen.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van elk element van `array` .

## <a name="example"></a>Voorbeeld

```qsharp
let unique1 = Unique(EqualI, [1, 1, 3, 3, 2, 5, 5, 5, 7]);
// same as [1, 3, 2, 5, 7]
let unique2 = Unique(EqualI, [2, 2, 1, 1, 2, 2, 1, 1]);
// same as [2, 1, 2, 1];
let unique3 = Unique(EqualI, Sorted(LessThanOrEqualI, [2, 2, 1, 1, 2, 2, 1, 1]));
// same as [1, 2];
```

## <a name="remarks"></a>Opmerkingen

Als er meerdere elementen zijn die gelijk zijn, maar niet naast elkaar staan, worden er meerdere exemplaren in de uitvoer matrix weer.  Gebruik deze functie samen met `Sorted` om een matrix met algemene unieke elementen op te halen.