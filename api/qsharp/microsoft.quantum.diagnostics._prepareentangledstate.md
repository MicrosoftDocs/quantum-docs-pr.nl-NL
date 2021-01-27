---
uid: Microsoft.Quantum.Diagnostics._prepareEntangledState
title: _prepareEntangledState bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _prepareEntangledState
qsharp.summary: >-
  Given two registers, prepares the maximally entangled state between each pair of qubits on the respective registers. All qubits must start in the |0⟩ state.

  The result is that corresponding pairs of qubits from each register are in the $\bra{\beta_{00}}\ket{\beta_{00}}$.
ms.openlocfilehash: 5a74978a536a92dafae0b532805bd8e8ae1c888e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830973"
---
# <a name="_prepareentangledstate-operation"></a>_prepareEntangledState bewerking

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Op basis van twee registers, wordt de status van de maximally Entangled voor elk paar qubits op de respectieve kassa's voor bereid.
Alle qubits moeten beginnen met de ⟩-status | 0.

Het resultaat is dat de bijbehorende paren qubits van elk REGI ster zich in de $ \bra{\ beta_ {00} } \ket{\ beta_ {00} } $ bevinden.

```qsharp
operation _prepareEntangledState (left : Qubit[], right : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="left--qubit"></a>links: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een Qubit-matrix in de $ \ket{0\cdots 0} $-status


### <a name="right--qubit"></a>rechts: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een Qubit-matrix in de $ \ket{0\cdots 0} $-status



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

