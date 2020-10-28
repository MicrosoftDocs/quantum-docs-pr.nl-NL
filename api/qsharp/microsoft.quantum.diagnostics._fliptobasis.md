---
uid: Microsoft.Quantum.Diagnostics._flipToBasis
title: _flipToBasis bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _flipToBasis
qsharp.summary: >-
  Applies unitaries that map $\ket{0}\otimes\cdots\ket{0}$ to $\ket{\psi_0} \otimes \ket{\psi_{n - 1}}$, where $\ket{\psi_k}$ depends on `basis[k]`.

  The correspondence between value of `basis[k]` and $\ket{\psi_k}$ is the following:

  - `basis[k]=0` $\rightarrow \ket{0}$. - `basis[k]=1` $\rightarrow \ket{1}$. - `basis[k]=2` $\rightarrow \ket{+}$. - `basis[k]=3` $\rightarrow \ket{i}$ ( +1 eigenstate of Pauli Y ).
ms.openlocfilehash: e074ed2ae259f6aef49a8d327ce518a9e2caebfa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702830"
---
# <a name="_fliptobasis-operation"></a>_flipToBasis bewerking

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


Past unitaries toe waarbij $ \ket {0} \otimes\cdots\ket {0} $ wordt toegewezen aan $ \ket{\ psi_0} \otimes \ket{\ psi_ {n-1}} $, waarbij $ \ket{\ psi_k} $ afhankelijk is van `basis[k]` .

De overeenkomst tussen de waarde van `basis[k]` en $ \ket{\ psi_k} $ is als volgt:

- `basis[k]=0` $ \rightarrow \ket {0} $.
- `basis[k]=1` $ \rightarrow \ket {1} $.
- `basis[k]=2` $ \rightarrow \ket{+} $.
- `basis[k]=3` $ \rightarrow \ket{i} $ (+ 1 eigenstate van Pauli Y).

```qsharp
operation _flipToBasis (basis : Int[], qubits : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="basis--int"></a>soort_jaar: [int](xref:microsoft.quantum.lang-ref.int)[]

Matrix van basis status-Id's van één Qubit (0 <= id <= 3), één voor elk element van qubits.


### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubit moet worden gebruikt.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

