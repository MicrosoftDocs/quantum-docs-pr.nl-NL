---
uid: Microsoft.Quantum.Arrays.ForEach
title: ForEach-bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ForEach
qsharp.summary: Given an array and an operation that is defined for the elements of the array, returns a new array that consists of the images of the original array under the operation.
ms.openlocfilehash: ab6ac6eb913095f31ba166ac27f034f2e2875acf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705997"
---
# <a name="foreach-operation"></a>ForEach-bewerking

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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