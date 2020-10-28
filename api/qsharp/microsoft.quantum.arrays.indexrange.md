---
uid: Microsoft.Quantum.Arrays.IndexRange
title: De functie IndexRange
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IndexRange
qsharp.summary: Given an array, returns a range over the indices of that array, suitable for use in a for loop.
ms.openlocfilehash: 7f9779acd4a781c50388217aa780710bd0b99ff3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705964"
---
# <a name="indexrange-function"></a>De functie IndexRange

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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