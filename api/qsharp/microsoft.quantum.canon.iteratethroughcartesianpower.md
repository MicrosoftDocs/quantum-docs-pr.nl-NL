---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Bewerking IterateThroughCartesianPower
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 526d28cbf3cd356b4f48eec02b3f032f70a868d9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704085"
---
# <a name="iteratethroughcartesianpower-operation"></a>Bewerking IterateThroughCartesianPower

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


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



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. IterateThroughCartesianProduct](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)