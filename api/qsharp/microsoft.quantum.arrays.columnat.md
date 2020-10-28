---
uid: Microsoft.Quantum.Arrays.ColumnAt
title: De functie ColumnAt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ColumnAt
qsharp.summary: Extracts a column from a matrix.
ms.openlocfilehash: ad09ada1a2253a54e70dddd6dba8aa243d2cd5a6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706165"
---
# <a name="columnat-function"></a>De functie ColumnAt

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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