---
uid: Microsoft.Quantum.Diagnostics._iterateThroughCartesianPower
title: _iterateThroughCartesianPower bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _iterateThroughCartesianPower
qsharp.summary: Iterates a variable through a Cartesian product [ 0, bounds[0]-1 ] × [ 0, bounds[1]-1 ] × [ 0, bounds[Length(bounds)-1]-1 ] and calls op(arr) for every element of the Cartesian product
ms.openlocfilehash: 36666238b40d036e3f6a8949b22f5806216d71f7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702825"
---
# <a name="_iteratethroughcartesianpower-operation"></a>_iterateThroughCartesianPower bewerking

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


Herhaalt een variabele via een Cartesisch product [0, grenzen [0]-1] × [0, grenzen [1]-1] x [0, grenzen [lengte (grenzen)-1]-1] en aanroepen op (arr) voor elk element van het Cartesisch product

```qsharp
operation _iterateThroughCartesianPower (length : Int, value : Int, op : (Int[] => Unit)) : Unit
```


## <a name="input"></a>Invoer

### <a name="length--int"></a>lengte: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="value--int"></a>waarde: [int](xref:microsoft.quantum.lang-ref.int)




### <a name="op--int--unit"></a>op: [int](xref:microsoft.quantum.lang-ref.int)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit) 





## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

