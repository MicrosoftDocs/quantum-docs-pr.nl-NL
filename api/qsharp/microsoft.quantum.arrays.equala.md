---
uid: Microsoft.Quantum.Arrays.EqualA
title: De functie equals
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EqualA
qsharp.summary: Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.
ms.openlocfilehash: 24fd76aaeb66081d6d8f1eaa3056117f54b5a5e7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706053"
---
# <a name="equala-function"></a>De functie equals

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


Op basis van twee matrices van hetzelfde type en een predikaat dat is gedefinieerd voor paren van elementen van de matrices, wordt gecontroleerd of de matrices gelijk zijn.

```qsharp
function EqualA<'T> (equal : (('T, 'T) -> Bool), array1 : 'T[], array2 : 'T[]) : Bool
```


## <a name="input"></a>Invoer

### <a name="equal--tt---bool"></a>gelijk aan: ('T, 'T)-> [BOOL](xref:microsoft.quantum.lang-ref.bool)

Een functie van tuple `('T, 'T)` naar `Bool` die wordt gebruikt om te controleren of twee elementen van matrices gelijk zijn.


### <a name="array1--t"></a>matrix1: 'T []

De eerste matrix die moet worden vergeleken.


### <a name="array2--t"></a>matrix2: ' []

De tweede matrix die moet worden vergeleken.



## <a name="output--bool"></a>Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)

De waarde `true` als en alleen als `array1` en `array2` gelijk zijn.
Dat wil zeggen, als beide matrices dezelfde lengte hebben en alle elementen gelijk zijn aan zoals gedefinieerd door `equal` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van de elementen van elke matrix.

## <a name="remarks"></a>Opmerkingen

Deze functie is gedefinieerd voor algemene typen. Wanneer we twee matrices `'T[]` en een functie hebben `equal: ('T, 'T) -> Bool` , retourneert deze functie dus een `Bool` waarde die aangeeft of de matrices gelijk zijn.
Als twee matrices als gelijk moeten worden beschouwd, moeten ze dezelfde lengte hebben en moeten de elementen in dezelfde posities in de matrices gelijk zijn.