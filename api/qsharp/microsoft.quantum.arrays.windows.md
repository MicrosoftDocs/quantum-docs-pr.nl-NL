---
uid: Microsoft.Quantum.Arrays.Windows
title: Windows-functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: 8f32a23aa4379744b84c3b8d9c8f565e61c3c64e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219886"
---
# <a name="windows-function"></a>Windows-functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert alle opeenvolgende submatrixen met een lengte `size` .

```qsharp
function Windows<'T> (size : Int, array : 'T[]) : 'T[][]
```


## <a name="description"></a>Beschrijving

Deze functie retourneert alle `n - size + 1` submatrixen met `size` een lengte in volg orde, waarbij `n` de lengte van is `arr` .
De eerste submatrixen bevinden zich `arr[0..size - 1], arr[1..size], arr[2..size + 1]` tot de laatste submatrix `arr[n - size..n - 1]` .

Als `size <= 0` of `size > n` , wordt een lege matrix geretourneerd.

## <a name="input"></a>Invoer

### <a name="size--int"></a>grootte: [int](xref:microsoft.quantum.lang-ref.int)

De lengte van de submatrixen.


### <a name="array--t"></a>matrix: 'T []

Een matrix met elementen.



## <a name="output--t"></a>Uitvoer: ' [] []



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type `array` elementen.