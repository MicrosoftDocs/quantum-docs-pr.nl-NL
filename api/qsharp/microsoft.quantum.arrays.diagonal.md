---
uid: Microsoft.Quantum.Arrays.Diagonal
title: Functie diagonaal
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Diagonal
qsharp.summary: Returns an array of diagonal elements of a 2-dimensional array
ms.openlocfilehash: fe6bac0acfa07b14620c7c35ae5e1cec2287d13d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221535"
---
# <a name="diagonal-function"></a>Functie diagonaal

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een matrix van diagonale elementen van een tweedimensionale matrix geretourneerd

```qsharp
function Diagonal<'T> (matrix : 'T[][]) : 'T[]
```


## <a name="description"></a>Beschrijving

Als de tweedimensionale matrix geen vier Kante vorm heeft, wordt de diagonaal boven het minimale aantal rijen en kolommen geretourneerd.

## <a name="input"></a>Invoer

### <a name="matrix--t"></a>matrix: ' [] []

2-dimensionale matrix in de volg orde van rijen



## <a name="output--t"></a>Uitvoer: ' []



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van elk element van `matrix` .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. arrays. getransponeerde](xref:Microsoft.Quantum.Arrays.Transposed)