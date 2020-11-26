---
uid: Microsoft.Quantum.Arrays.IndexRange
title: De functie IndexRange
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 5afd4cc260ac3e384d2736bf7b43d941afd9ef73
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220940"
---
# <a name="indexrange-function"></a>De functie IndexRange

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Op basis van een matrix, retourneert een bereik over de indices van die matrix, die geschikt is voor gebruik in een for-lus.

```qsharp
function IndexRange<'TElement> (array : 'TElement[]) : Range
```


## <a name="input"></a>Invoer

### <a name="array--telement"></a>matrix: ' TEle []

Een matrix waarvoor een reeks indexen moet worden geretourneerd.



## <a name="output--range"></a>Uitvoer: [bereik](xref:microsoft.quantum.lang-ref.range)

Een bereik van alle indices van de matrix.

## <a name="type-parameters"></a>Type parameters

### <a name="telement"></a>-TEle

Het type elementen van de matrix.