---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: Bewerking IterateThroughCartesianProduct
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: e4fc71f6f707639f6f89eece8546ec2fb434a15a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704093"
---
# <a name="iteratethroughcartesianproduct-operation"></a>Bewerking IterateThroughCartesianProduct

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


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