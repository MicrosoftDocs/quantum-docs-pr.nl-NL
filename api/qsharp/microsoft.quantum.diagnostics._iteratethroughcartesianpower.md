---
uid: Microsoft.Quantum.Diagnostics._iterateThroughCartesianPower
title: _iterateThroughCartesianPower bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _iterateThroughCartesianPower
qsharp.summary: Iterates a variable through a Cartesian product [ 0, bounds[0]-1 ] × [ 0, bounds[1]-1 ] × [ 0, bounds[Length(bounds)-1]-1 ] and calls op(arr) for every element of the Cartesian product
ms.openlocfilehash: cde25eb99c9e1bde080c5356ecabd9f12cde9bba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213715"
---
# <a name="_iteratethroughcartesianpower-operation"></a>_iterateThroughCartesianPower bewerking

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Herhaalt een variabele via een Cartesisch product [0, grenzen [0]-1] × [0, grenzen [1]-1] x [0, grenzen [lengte (grenzen)-1]-1] en aanroepen op (arr) voor elk element van het Cartesisch product

```qsharp
operation _iterateThroughCartesianPower (length : Int, value : Int, op : (Int[] => Unit)) : Unit
```


## <a name="input"></a>Invoer

### <a name="length--int"></a>lengte: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="value--int"></a>waarde: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="op--int--unit"></a>op: [int](xref:microsoft.quantum.lang-ref.int)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit) 





## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

