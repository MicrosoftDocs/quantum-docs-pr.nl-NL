---
uid: Microsoft.Quantum.Arrays.Transposed
title: Getransponeerde functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: f293399d8e3a2cb32b2929e8d1591ac5eaefd277
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219988"
---
# <a name="transposed-function"></a>Getransponeerde functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert de getransponeerde matrix die wordt weer gegeven als een matrix met matrices.

```qsharp
function Transposed<'T> (matrix : 'T[][]) : 'T[][]
```


## <a name="description"></a>Beschrijving

Invoer als $r \times c $ matrix met $r $ rows en $c $ columns.  De matrix is gebaseerd op rijen, dat wil zeggen, `matrix[i][j]` het element op rij $i $ en kolom $j $.

Deze functie retourneert de $c \times r $ matrix die de getransponeerde van de invoer matrix is.

## <a name="input"></a>Invoer

### <a name="matrix--t"></a>matrix: ' [] []

Op rijen gebaseerd $r \times c $ matrix



## <a name="output--t"></a>Uitvoer: ' [] []

$C \times r $ matrix getransponeerd

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van elk element van `matrix` .