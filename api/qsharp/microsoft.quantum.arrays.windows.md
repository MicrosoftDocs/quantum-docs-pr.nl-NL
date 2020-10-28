---
uid: Microsoft.Quantum.Arrays.Windows
title: Windows-functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: Windows
qsharp.summary: Returns all consecutive subarrays of length `size`.
ms.openlocfilehash: 6071d1c3e5981855c57abd0e741b1de0201c30a3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705693"
---
# <a name="windows-function"></a>Windows-functie

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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