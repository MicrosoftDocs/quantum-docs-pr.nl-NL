---
uid: Microsoft.Quantum.Arrays.EqualA
title: De functie equals
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EqualA
qsharp.summary: Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.
ms.openlocfilehash: 176e15139a27d375fb047c07fa1ee778dc8cc2ce
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221365"
---
# <a name="equala-function"></a>De functie equals

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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