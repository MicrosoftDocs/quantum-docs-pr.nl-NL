---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Bewerking IterateThroughCartesianPower
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 3a303d13c4a6f102dab92d814e24df9d90213fbe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840298"
---
# <a name="iteratethroughcartesianpower-operation"></a>Bewerking IterateThroughCartesianPower

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Past een bewerking toe voor elke index in het Cartesisch vermogen van een bereik met gehele getallen.

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a>Beschrijving

Hiermee wordt een bewerking uitgevoerd voor elk element van een Cartesisch vermogen van het bereik `0..(bound - 1)` .

## <a name="input"></a>Invoer

### <a name="power--int"></a>energie: [int](xref:microsoft.quantum.lang-ref.int)

Het Cartesisch vermogen waarmee het bereik `0..(bound - 1)` moet worden verhoogd.


### <a name="bound--int"></a>gebonden: [int](xref:microsoft.quantum.lang-ref.int)

Een specificatie van het bereik dat moet worden herhaald, opgegeven als de lengte van het bereik.


### <a name="op--int--unit"></a>op: [int](xref:microsoft.quantum.lang-ref.int)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een bewerking die moet worden aangeroepen voor elk element van het opgegeven Cartesisch vermogen.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="example"></a>Voorbeeld

Op basis van een bewerking `op` zijn de volgende twee fragmenten gelijk:

```qsharp
IterateThroughCartesianPower(2, 3, op);
```

```qsharp
op([0, 0]);
op([1, 0]);
op([2, 0]);
op([0, 1]);
// ..
op([2, 2]);
```

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. IterateThroughCartesianProduct](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)