---
uid: Microsoft.Quantum.Arrays.MappedByIndex
title: De functie MappedByIndex
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedByIndex
qsharp.summary: Given an array and a function that is defined for the indexed elements of the array, returns a new array that consists of the images of the original array under the function.
ms.openlocfilehash: 430495517974b641c249fa146aa9effec542e825
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209924"
---
# <a name="mappedbyindex-function"></a>De functie MappedByIndex

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Op basis van een matrix en een functie die is gedefinieerd voor de geïndexeerde elementen van de matrix, retourneert een nieuwe matrix die bestaat uit de installatie kopieën van de oorspronkelijke matrix onder de functie.

```qsharp
function MappedByIndex<'T, 'U> (mapper : ((Int, 'T) -> 'U), array : 'T[]) : 'U[]
```


## <a name="input"></a>Invoer

### <a name="mapper--intt---u"></a>Mapper: ([int](xref:microsoft.quantum.lang-ref.int), 't)-> ' U

Een functie van `(Int, 'T)` naar `'U` die wordt gebruikt om elementen en hun indices toe te wijzen.


### <a name="array--t"></a>matrix: 'T []

Een matrix van elementen `'T` .



## <a name="output--u"></a>Uitvoer: ' U []

Een matrix `'U[]` van elementen die worden toegewezen door de `mapper` functie.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type `array` elementen.
### <a name="u"></a>' U

Het resultaat type van de `mapper` functie.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. arrays. toegewezen](xref:Microsoft.Quantum.Arrays.Mapped)