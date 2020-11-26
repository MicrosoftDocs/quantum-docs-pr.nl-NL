---
uid: Microsoft.Quantum.Arrays.Mapped
title: Toegewezen functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Mapped
qsharp.summary: Given an array and a function that is defined for the elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 9632b9f53ffad8ece958ab1dc9ad446c7dcb9e13
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220736"
---
# <a name="mapped-function"></a>Toegewezen functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een matrix en een functie die is gedefinieerd voor de elementen van de matrix, retourneert een nieuwe matrix die bestaat uit de installatie kopieën van de oorspronkelijke matrix onder de functie.

```qsharp
function Mapped<'T, 'U> (mapper : ('T -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a>Invoer

### <a name="mapper--t---u"></a>Mapper: 'T-> ' U

Een functie van `'T` naar `'U` die wordt gebruikt voor het toewijzen van elementen.


### <a name="array--t"></a>matrix: 'T []

Een matrix van elementen `'T` .



## <a name="output--u"></a>Uitvoer: ' U []

Een matrix `'U[]` van elementen die worden toegewezen door de `mapper` functie.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type `array` elementen.
### <a name="u"></a>' U

Het resultaat type van de `mapper` functie.

## <a name="remarks"></a>Opmerkingen

De functie is gedefinieerd voor algemene typen, dat wil zeggen, wanneer we een matrix hebben `'T[]` en een functie `mapper: 'T -> 'U` die we de elementen van de matrix kunnen toewijzen en een nieuwe matrix van het type produceren `'U[]` .