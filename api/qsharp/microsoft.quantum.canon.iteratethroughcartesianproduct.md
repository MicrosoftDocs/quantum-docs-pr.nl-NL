---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: Bewerking IterateThroughCartesianProduct
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: a0aaa8ef6aa6798d31c810254c92820f8136800c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840283"
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



## <a name="example"></a>Voorbeeld

Op basis van een bewerking `op` zijn de volgende twee fragmenten gelijk:

```qsharp
IterateThroughCartesianProduct([3, 4, 5], op);
```

```qsharp
op([0, 0, 0]);
op([1, 0, 0]);
op([2, 0, 0]);
op([0, 1, 0]);
// ...
op([0, 3, 0]);
op([0, 0, 1]);
//
op([2, 3, 4]);
```

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. IterateThroughCartesianPower](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)