---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: De functie ColumnAt
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: 097b3fdd6fc1843ada27052fcf08ee80d894d25a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210095"
---
# <a name="columnat-function"></a>De functie ColumnAt

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een kolom uit een matrix opgehaald.

```qsharp
function ColumnAt<'T> (column : Int, matrix : 'T[][]) : 'T[]
```


## <a name="description"></a>Beschrijving

Met deze functie wordt een kolom in een matrix geëxtraheerd in de volg orde van rijen.
Het extra heren van een rij-corrsponds om toegang te krijgen tot elementen van de eerste index. hiervoor is daarom geen verdere behandeling vereist.

## <a name="input"></a>Invoer

### <a name="column--int"></a>kolom: [int](xref:microsoft.quantum.lang-ref.int)

Kolom van de matrix


### <a name="matrix--t"></a>matrix: ' [] []

2-dimensionale matrix in de volg orde van rijen



## <a name="output--t"></a>Uitvoer: ' []



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van elk element van `matrix` .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. arrays. getransponeerde](xref:Microsoft.Quantum.Arrays.Transposed)
- [Micro soft. Quantum. arrays. diagonaal](xref:Microsoft.Quantum.Arrays.Diagonal)