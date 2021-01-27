---
uid: Microsoft.Quantum.Arrays.MostAndTail
title: De functie MostAndTail
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: MostAndTail
qsharp.summary: Returns a tuple of all but one and the last element of the array.
ms.openlocfilehash: fd5569f1b71ac2fdf2b5c08ba7dde172e3a6744e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845593"
---
# <a name="mostandtail-function"></a>De functie MostAndTail

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een tuple van alle, maar één en het laatste element van de matrix.

```qsharp
function MostAndTail<'A> (array : 'A[]) : ('A[], 'A)
```


## <a name="input"></a>Invoer

### <a name="array--a"></a>matrix: ' A []

Een matrix met ten minste één element.



## <a name="output--aa"></a>Output: (' A [], ' A)

Een tuple van alle, maar één en het laatste element van de matrix.

## <a name="type-parameters"></a>Type parameters

### <a name="a"></a>' A

Het type van de matrix elementen.