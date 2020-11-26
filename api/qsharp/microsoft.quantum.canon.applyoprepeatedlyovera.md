---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverA
title: Bewerking ApplyOpRepeatedlyOverA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverA
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 65675a3a83f0ac730b9e3a58f80f77c096c1ce57
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209142"
---
# <a name="applyoprepeatedlyovera-operation"></a>Bewerking ApplyOpRepeatedlyOverA

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Past hetzelfde op een Qubit-REGI ster meerdere keren toe.

```qsharp
operation ApplyOpRepeatedlyOverA (op : (Qubit[] => Unit is Adj), targets : Int[][], register : Qubit[]) : Unit is Adj
```


## <a name="input"></a>Invoer

### <a name="op--qubit--unit--is-adj"></a>op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ

Een bewerking die meerdere keren wordt toegepast op het Qubit-REGI ster


### <a name="targets--int"></a>doelen: [int](xref:microsoft.quantum.lang-ref.int)[] []

Geneste matrices waarin de doelen van de op-op worden beschreven. Elke matrix moet een lijst bevatten met ints die het qubits beschrijven dat moet worden gebruikt.


### <a name="register--qubit"></a>registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubit-REGI ster waarop moet worden gehandeld.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Canon. ApplySeriesOfOps](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)