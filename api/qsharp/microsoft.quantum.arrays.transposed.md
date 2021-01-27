---
uid: Microsoft.Quantum.Arrays.Transposed
title: Getransponeerde functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Transposed
qsharp.summary: Returns the transpose of a matrix represented as an array of arrays.
ms.openlocfilehash: 913f1829ef53ec3eb6944be8b8e3eb37b431f27e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850937"
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

## <a name="example"></a>Voorbeeld

```qsharp
// same as [[1, 4], [2, 5], [3, 6]]
let transposed = Transposed([[1, 2, 3], [4, 5, 6]]);
```