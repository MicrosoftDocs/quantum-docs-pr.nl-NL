---
uid: Microsoft.Quantum.Arrays.Filtered
title: Gefilterde functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Filtered
qsharp.summary: Given an array and a predicate that is defined for the elements of the array, returns an array that consists of those elements that satisfy the predicate.
ms.openlocfilehash: 83336b7001ce1d8ab1f5340b194abdcf93588c31
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847168"
---
# <a name="filtered-function"></a>Gefilterde functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een matrix en een predikaat die is gedefinieerd voor de elementen van de matrix, retourneert een matrix die bestaat uit die elementen die voldoen aan het predicaat.

```qsharp
function Filtered<'T> (predicate : ('T -> Bool), array : 'T[]) : 'T[]
```


## <a name="input"></a>Invoer

### <a name="predicate--t---bool"></a>predikaat: niet-> [BOOL](xref:microsoft.quantum.lang-ref.bool)

Een functie van `'T` naar een Booleaanse waarde die wordt gebruikt voor het filteren van elementen.


### <a name="array--t"></a>matrix: 'T []

Een matrix van elementen `'T` .



## <a name="output--t"></a>Uitvoer: ' []

Een matrix `'T[]` met elementen die voldoen aan het predicaat.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type `array` elementen.

## <a name="example"></a>Voorbeeld

De volgende code toont de functie ' gefilterd '.
Een predikaat is gedefinieerd met behulp van de @"microsoft.quantum.logical.greaterthani" functie:

```qsharp
open Microsoft.Quantum.Arrays;
open Microsoft.Quantum.Logical;

function FilteredDemo() : Unit {
   let predicate = GreaterThanI(_, 5);
   let filteredArray = Filtered(predicate, [2, 5, 9, 1, 8]);
   Message($"{filteredArray}");
}
```

Het resultaat dat één moet verwachten van dit voor beeld is een matrix met getallen die groter is dan 5.

## <a name="remarks"></a>Opmerkingen

De functie is gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix `'T[]` en een predikaat hebben waarop `'T -> Bool` we elementen kunnen filteren.