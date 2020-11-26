---
uid: Microsoft.Quantum.Arrays.Chunks
title: De functie chunks
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Chunks
qsharp.summary: Splits an array into multiple parts of equal length.
ms.openlocfilehash: b323fdab1b207c72a4f46d5ca4cb368ecf0df818
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221603"
---
# <a name="chunks-function"></a>De functie chunks

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Splitst een matrix in meerdere delen van gelijke lengte.

```qsharp
function Chunks<'T> (nElements : Int, arr : 'T[]) : 'T[][]
```


## <a name="input"></a>Invoer

### <a name="nelements--int"></a>nElements: [int](xref:microsoft.quantum.lang-ref.int)

De lengte van elk segment.


### <a name="arr--t"></a>ARR: 'T []

De matrix die moet worden gesplitst.



## <a name="output--t"></a>Uitvoer: ' [] []

Een matrix met elk segment van de oorspronkelijke matrix.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T



## <a name="remarks"></a>Opmerkingen

Houd er rekening mee dat het laatste element van de uitvoer mogelijk korter `nElements` is dan of `Length(arr)` niet deelbaar is door `nElements` .