---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver
title: Bewerking ApplyOpRepeatedlyOver
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOver
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 263eff8ec31f5ee36485eb1d2ed52bf15cef4bef
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844803"
---
# <a name="applyoprepeatedlyover-operation"></a>Bewerking ApplyOpRepeatedlyOver

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Past hetzelfde op een Qubit-REGI ster meerdere keren toe.

```qsharp
operation ApplyOpRepeatedlyOver (op : (Qubit[] => Unit), targets : Int[][], register : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="op--qubit--unit"></a>op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit) 

Een bewerking die meerdere keren wordt toegepast op het Qubit-REGI ster


### <a name="targets--int"></a>doelen: [int](xref:microsoft.quantum.lang-ref.int)[] []

Geneste matrices waarin de doelen van de op-op worden beschreven. Elke matrix moet een lijst bevatten met ints die het qubits beschrijven dat moet worden gebruikt.


### <a name="register--qubit"></a>registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubit-REGI ster waarop moet worden gehandeld.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplySeriesOfOps](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)