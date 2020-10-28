---
uid: Microsoft.Quantum.Arrays.Unique
title: Unieke functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Unique
qsharp.summary: Returns a new array that has no equal adjacent elements.
ms.openlocfilehash: c5d40bb82f2de640e9c78eef0c27e4766b477826
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705717"
---
# <a name="unique-function"></a>Unieke functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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

## <a name="remarks"></a>Opmerkingen

Als er meerdere elementen zijn die gelijk zijn, maar niet naast elkaar staan, worden er meerdere exemplaren in de uitvoer matrix weer.  Gebruik deze functie samen met `Sorted` om een matrix met algemene unieke elementen op te halen.