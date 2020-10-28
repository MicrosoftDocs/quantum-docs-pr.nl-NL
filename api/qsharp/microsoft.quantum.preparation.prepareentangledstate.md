---
uid: Microsoft.Quantum.Preparation.PrepareEntangledState
title: Bewerking PrepareEntangledState
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Preparation
qsharp.name: PrepareEntangledState
qsharp.summary: >-
  Pairwise entangles two qubit registers.

  That is, given two registers, prepares the maximally entangled state $\frac{1}{\sqrt{2}} \left(\ket{00} + \ket{11} \right)$ between each pair of qubits on the respective registers, assuming that each register starts in the $\ket{0\cdots 0}$ state.
ms.openlocfilehash: 299d586f7581acdecf22da2f6bbfbb8d45f372f3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707867"
---
# <a name="prepareentangledstate-operation"></a>Bewerking PrepareEntangledState

Naam ruimte: [micro soft. Quantum. prepare](xref:Microsoft.Quantum.Preparation)

Pakket [](https://nuget.org/packages/)


Pairwise entangles twee Qubit-registers.

Op basis van twee registers wordt de maximally Entangled-status $ \frac {1} {\sqrt {2} } \left (\ket {00} + \ket {11} \right) $ tussen elk paar qubits op de respectieve kassa's voor bereid, ervan uitgaande dat elke kassa begint met de status $ \ket{0\cdots 0} $.

```qsharp
operation PrepareEntangledState (left : Qubit[], right : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="left--qubit"></a>links: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een Qubit-matrix in de $ \ket{0\cdots 0} $-status


### <a name="right--qubit"></a>rechts: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een Qubit-matrix in de $ \ket{0\cdots 0} $-status



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

