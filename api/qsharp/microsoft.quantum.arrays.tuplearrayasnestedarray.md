---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: De functie TupleArrayAsNestedArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: 917f35db949790ab3ae6e7a2184bcfcf5ed50be6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705733"
---
# <a name="tuplearrayasnestedarray-function"></a>De functie TupleArrayAsNestedArray

Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)

Pakket [](https://nuget.org/packages/)


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

