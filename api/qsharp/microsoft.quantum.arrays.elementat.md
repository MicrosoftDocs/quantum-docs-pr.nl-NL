---
uid: Microsoft.Quantum.Arrays.ElementAt
title: De functie ElementAt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ElementAt
qsharp.summary: Returns the at the given index of an array.
ms.openlocfilehash: 2d31c62a4a5ba3b273e7440b5dfe4482b47e3a8b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842805"
---
# <a name="elementat-function"></a>De functie ElementAt

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert de opgegeven index van een matrix.

```qsharp
function ElementAt<'T> (index : Int, array : 'T[]) : 'T
```


## <a name="input"></a>Invoer

### <a name="index--int"></a>index: [int](xref:microsoft.quantum.lang-ref.int)

Index van element


### <a name="array--t"></a>matrix: 'T []

De matrix die wordt geïndexeerd.



## <a name="output--t"></a>Uitvoer: 'T



## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

Het type van elk element van `array` .

## <a name="example"></a>Voorbeeld

Haal het derde getal op in vier beroemde gehele getallen. (Houd er rekening mee dat de 0-index overeenkomt met de _eerste_ waarde van de reeks.)

```qsharp
let lucas = [2, 1, 3, 4, 7, 11, 18, 29, 47, 76];
let prime = [2, 3, 5, 7, 11, 13, 17, 19, 23, 29];
let fibonacci = [0, 1, 1, 2, 3, 5, 8, 13, 21, 34];
let catalan = [1, 1, 2, 5, 14, 42, 132, 429, 1430, 4862];
let famous2 = Mapped(ElementAt<Int>(2, _), [lucas, prime, fibonacci, catalan]);
// same as: famous2 = [3, 5, 1, 2]
```

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. arrays. LookupFunction](xref:Microsoft.Quantum.Arrays.LookupFunction)
- [Micro soft. Quantum. arrays. ElementsAt](xref:Microsoft.Quantum.Arrays.ElementsAt)