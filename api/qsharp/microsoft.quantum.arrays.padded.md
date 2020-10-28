---
uid: Microsoft.Quantum.Arrays.Padded
title: Functie aangevuld
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Padded
qsharp.summary: Returns an array padded at with specified values up to a specified length.
ms.openlocfilehash: 8742d4726e7ee32349bf3d0bd5077352ffca350b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705852"
---
# <a name="padded-function"></a>Functie aangevuld

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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