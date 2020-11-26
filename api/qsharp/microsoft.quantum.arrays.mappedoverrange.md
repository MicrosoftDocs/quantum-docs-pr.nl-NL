---
uid: Microsoft.Quantum.Arrays.MappedOverRange
title: De functie MappedOverRange
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MappedOverRange
qsharp.summary: Given a range and a function that takes an integer as input, returns a new array that consists of the images of the range values under the function.
ms.openlocfilehash: b1d73c2503e63ed09a3d6a56421760ca29eb0c3f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220685"
---
# <a name="mappedoverrange-function"></a>De functie MappedOverRange

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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