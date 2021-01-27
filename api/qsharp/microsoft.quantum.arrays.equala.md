---
uid: Microsoft.Quantum.Arrays.EqualA
title: De functie equals
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: EqualA
qsharp.summary: Given two arrays of the same type and a predicate that is defined for pairs of elements of the arrays, checks whether the arrays are equal.
ms.openlocfilehash: fe22e208f67d2c289b0b2d99f19ff26fc5abc3d8
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848693"
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

## <a name="example"></a>Voorbeeld

Met de volgende code wordt gecontroleerd of verschillende matrix paren gelijk zijn:

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function EqualADemo() : Unit {
    let equalArrays = EqualA(EqualI, [2, 3, 4], [2, 3, 4]);
    let differentLength = EqualA(EqualD, [2.0, 3.0, 4.0], [2.0, 3.0]);
    let differentElements = EqualA(EqualR, [One, Zero], [One, One]);
    Message($"Equal arrays are {equalArrays ? "equal" | "not equal"}");
    Message($"Arrays of different length are {differentLength ? "equal" | "not equal"}");
    Message($"Arrays of the same length with different elements are {differentElements ? "equal" | "not equal"}");
}
```

## <a name="remarks"></a>Opmerkingen

Deze functie is gedefinieerd voor algemene typen. Wanneer we twee matrices `'T[]` en een functie hebben `equal: ('T, 'T) -> Bool` , retourneert deze functie dus een `Bool` waarde die aangeeft of de matrices gelijk zijn.
Als twee matrices als gelijk moeten worden beschouwd, moeten ze dezelfde lengte hebben en moeten de elementen in dezelfde posities in de matrices gelijk zijn.