---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: De functie TupleArrayAsNestedArray
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: 51a35555080d1d2475fc1aa9e48e84c7c6f92c51
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845397"
---
# <a name="tuplearrayasnestedarray-function"></a>De functie TupleArrayAsNestedArray

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een lijst met 2-Tuples omgezet in een geneste matrix.

```qsharp
function TupleArrayAsNestedArray<'T> (tupleList : ('T, 'T)[]) : 'T[][]
```


## <a name="input"></a>Invoer

### <a name="tuplelist--tt"></a>tupleList: ('T, 'T) []

Lijst met twee Tuples die moeten worden omgezet in een geneste matrix.



## <a name="output--t"></a>Uitvoer: ' [] []

Een geneste matrix met een lengte die overeenkomt met de tupleList.

## <a name="example"></a>Voorbeeld

```qsharp
// The following returns [[2, 3], [4, 5]]
TupleArrayAsNestedArray([(2, 3), (4, 5)]);
```

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

