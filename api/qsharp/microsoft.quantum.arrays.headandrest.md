---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: De functie HeadAndRest
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: 9af4ba48a21d3cdf932b2f702051a70a6108db1b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705981"
---
# <a name="headandrest-function"></a>De functie HeadAndRest

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


Retourneert een tuple van de eerste en alle resterende elementen van de matrix.

```qsharp
function HeadAndRest<'A> (array : 'A[]) : ('A, 'A[])
```


## <a name="input"></a>Invoer

### <a name="array--a"></a>matrix: ' A []

Een matrix met ten minste één element.



## <a name="output--aa"></a>Uitvoer: (' A ', ' A [])

Een tuple van de eerste en alle resterende elementen van de matrix.

## <a name="type-parameters"></a>Type parameters

### <a name="a"></a>' A

Het type van de matrix elementen.