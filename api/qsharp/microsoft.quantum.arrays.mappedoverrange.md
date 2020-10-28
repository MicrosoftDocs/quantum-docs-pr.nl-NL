---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: De functie MappedOverRange
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: e527a3ca1fd7571836f4f79bb453581f53d1db2b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705892"
---
# <a name="mappedoverrange-function"></a>De functie MappedOverRange

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


Op basis van een bereik en een functie die een geheel getal als invoer accepteert, retourneert een nieuwe matrix die bestaat uit de afbeeldingen van de bereik waarden onder de functie.

```qsharp
function MappedOverRange<'T> (mapper : (Int -> 'T), range : Range) : 'T[]
```


## <a name="input"></a>Invoer

### <a name="mapper--int---t"></a>Mapper: [int](xref:microsoft.quantum.lang-ref.int) -> niet

Een functie van `Int` naar `'T` die wordt gebruikt om bereik waarden toe te wijzen.


### <a name="range--range"></a>bereik: [bereik](xref:microsoft.quantum.lang-ref.range)

Een bereik van gehele getallen.



## <a name="output--t"></a>Uitvoer: ' []

Een matrix `'T[]` van elementen die worden toegewezen door de `mapper` functie.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het resultaat type van de `mapper` functie.

## <a name="remarks"></a>Opmerkingen

De functie is gedefinieerd voor algemene typen, d.w.z. Wanneer we een functie hebben, `mapper: Int -> 'T` kunnen we de waarden van het bereik toewijzen en een matrix van het type produceren `'T[]` .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. arrays. toegewezen](xref:Microsoft.Quantum.Arrays.Mapped)