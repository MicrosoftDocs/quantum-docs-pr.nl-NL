---
uid: Microsoft.Quantum.Diagnostics._prepareEntangledState
title: _prepareEntangledState bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _prepareEntangledState
qsharp.summary: >-
  Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers. All qubits must start in the |0⟩ state.

  The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.
ms.openlocfilehash: 384dad5905cec50b500028e1bc352a742122b299
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702824"
---
# <a name="_prepareentangledstate-operation"></a>_prepareEntangledState bewerking

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


Op basis van twee registers, wordt de status van de maximally Entangled voor elk paar qubits op de respectieve kassa's voor bereid.
Alle qubits moeten beginnen met de ⟩-status | 0.

Het resultaat is dat de bijbehorende paren qubits van elk REGI ster zich in de $ \bra{\ beta_ {00} } \ket{\ beta_ {00} } $ bevinden.

```qsharp
operation _prepareEntangledState (left : Qubit[], right : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="left--qubit"></a>links: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een Qubit-matrix in de $ \ket{0\cdots 0} $-status


### <a name="right--qubit"></a>rechts: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een Qubit-matrix in de $ \ket{0\cdots 0} $-status



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

