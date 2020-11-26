---
uid: Microsoft.Quantum.Arrays.HeadAndRest
title: De functie HeadAndRest
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: HeadAndRest
qsharp.summary: Returns a tuple of first and all remaining elements of the array.
ms.openlocfilehash: 1144e00227df1cd7d96bc76b118b0b556adbaa96
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221076"
---
# <a name="headandrest-function"></a>De functie HeadAndRest

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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