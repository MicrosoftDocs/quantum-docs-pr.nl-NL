---
uid: Microsoft.Quantum.Arrays.ForEach
title: ForEach-bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: b362d28e77c8dea2b3daeed4a4d605e1dd42e487
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221144"
---
# <a name="foreach-operation"></a>ForEach-bewerking

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een matrix en een bewerking die is gedefinieerd voor de elementen van de matrix, retourneert een nieuwe matrix die bestaat uit de installatie kopieën van de oorspronkelijke matrix onder de bewerking.

```qsharp
operation ForEach<'T, 'U> (action : ('T => 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a>Invoer

### <a name="action--t--u"></a>actie: 'T => ' U 

Een bewerking van `'T` naar `'U` die wordt toegepast op elk element.


### <a name="array--t"></a>matrix: 'T []

Een matrix van elementen `'T` .



## <a name="output--u"></a>Uitvoer: ' U []

Een matrix `'U[]` met elementen die worden toegewezen door de `action` bewerking.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type `array` elementen.
### <a name="u"></a>' U

Het resultaat type van de `action` bewerking.

## <a name="remarks"></a>Opmerkingen

De bewerking wordt gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix `'T[]` en een bewerking hebben `action : 'T -> 'U` die de elementen van de matrix kunnen toewijzen en een nieuwe matrix van het type maken `'U[]` .