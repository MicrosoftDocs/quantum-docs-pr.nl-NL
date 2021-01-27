---
uid: Microsoft.Quantum.Arrays.Padded
title: Functie aangevuld
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 556e5f5175ee54470a99f32c037eeb2cd80588d0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845566"
---
# <a name="padded-function"></a>Functie aangevuld

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een matrix met de opgegeven waarden tot een opgegeven lengte.

```qsharp
function Padded<'T> (nElementsTotal : Int, defaultElement : 'T, inputArray : 'T[]) : 'T[]
```


## <a name="input"></a>Invoer

### <a name="nelementstotal--int"></a>nElementsTotal: [int](xref:microsoft.quantum.lang-ref.int)

De lengte van de opgevulde matrix. Als dit positief is, `inputArray` wordt aan het hoofd opgevuld. Als dit negatief is, `inputArray` wordt aan de staart opgevuld.


### <a name="defaultelement--t"></a>defaultElement: 'T

Standaard waarde voor het gebruik van opvullings elementen.


### <a name="inputarray--t"></a>inputArray: 'T []

Matrix waarvan de waarden zich op het hoofd van de uitvoer matrix bevinden.



## <a name="output--t"></a>Uitvoer: ' []

Een matrix `output` die de `inputArray` opgevulde waarde bij het hoofd met `defaultElement` s tot een `output` lengte heeft `nElementsTotal`

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van de matrix elementen.

## <a name="example"></a>Voorbeeld

```qsharp
let array = [10, 11, 12];
// The following line returns [10, 12, 15, 2, 2, 2].
let output = Padded(-6, array, 2);
// The following line returns [2, 2, 2, 10, 12, 15].
let output = Padded(6, array, 2);
```