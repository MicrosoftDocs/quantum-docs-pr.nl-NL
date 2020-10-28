---
uid: Microsoft.Quantum.Arrays.Subarray
title: Submatrix functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Subarray
qsharp.summary: Takes an array and a list of locations and produces a new array formed from the elements of the original array that match the given locations.
ms.openlocfilehash: be7b6ee1a396d67ebc311d8d97f4bd751a32d171
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705757"
---
# <a name="subarray-function"></a>Submatrix functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


Neemt een matrix en een lijst met locaties en produceert een nieuwe matrix die is samengesteld op basis van de elementen van de oorspronkelijke matrix die overeenkomen met de opgegeven locaties.

```qsharp
function Subarray<'T> (indices : Int[], array : 'T[]) : 'T[]
```


## <a name="input"></a>Invoer

### <a name="indices--int"></a>indices: [int](xref:microsoft.quantum.lang-ref.int)[]

Een lijst met gehele getallen die wordt gebruikt voor het definiëren van de submatrix.


### <a name="array--t"></a>matrix: 'T []

Een matrix van elementen `'T` .



## <a name="output--t"></a>Uitvoer: ' []

Een matrix `out` met elementen waarvan de indices overeenkomen met de submatrix, dat wil zeggen `out[idx] == array[indices[idx]]` .

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type `array` elementen.

## <a name="remarks"></a>Opmerkingen

De functie is gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix hebben `'T[]` en een lijst met locaties `Int[]` waarmee de submatrix wordt gedefinieerd.
De constructie van de submatrix is een gebaseerd op het genereren van een nieuwe, diep gaande kopie van de opgegeven matrix in plaats van verwijzingen te onderhouden.

Als `Length(indices) < Length(array)` deze functie een subset retourneert, wordt geretourneerd `array` . Als er daarentegen `indices` herhaalde elementen bevatten, worden ook de bijbehorende elementen van `array` herhaald.
Als `indices` en `array` dezelfde lengte hebben, biedt deze functie permutaties van `array` .