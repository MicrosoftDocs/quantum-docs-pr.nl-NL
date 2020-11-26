---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: Bewerking IterateThroughCartesianProduct
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: 6340c7a972253e6f583a3856df93a7066ced3139
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206439"
---
# <a name="iteratethroughcartesianproduct-operation"></a>Bewerking IterateThroughCartesianProduct

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Past een bewerking toe voor elke index in het Cartesisch product van verschillende bereiken.

```qsharp
operation IterateThroughCartesianProduct (bounds : Int[], op : (Int[] => Unit)) : Unit
```


## <a name="description"></a>Beschrijving

Hiermee wordt een bewerking uitgevoerd voor elk element van het Cartesisch product van `0..(bounds[0] - 1)` , `0..(bounds[1] - 1)` ,,..., `0..(bounds[Length(bounds) - 1] - 1)`

## <a name="input"></a>Invoer

### <a name="bounds--int"></a>grenzen: [int](xref:microsoft.quantum.lang-ref.int)[]

Een matrix die de bereiken specificeert die moeten worden herhaald, waarbij elk bereik wordt opgegeven als een integer lengte.


### <a name="op--int--unit"></a>op: [int](xref:microsoft.quantum.lang-ref.int)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een bewerking die moet worden aangeroepen voor elk element van het opgegeven Cartesisch product.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. IterateThroughCartesianPower](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)