---
uid: Microsoft.Quantum.Intrinsic.Exp
title: EXP-bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Exp
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator.

  \begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: b923374a954f90aba2deaead79dd419fbf67fea3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702134"
---
# <a name="exp-operation"></a>EXP-bewerking

Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)

Pakket [](https://nuget.org/packages/)


Past de exponentiële waarde van een multi-Qubit Pauli-operator toe.

\begin{align} e ^ {i \theta [P_0 \otimes P_1 \cdots P_ {N-1}]}, \end{align} waarbij $P _i $ het $i $ TH element van is `paulis` en waar $N = $ `Length(paulis)` .

```qsharp
operation Exp (paulis : Pauli[], theta : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="paulis--pauli"></a>PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Matrix van Pauli-waarden met één Qubit die de tensor-product factoren op elke qubit aangeven.


### <a name="theta--double"></a>Theta: [dubbel](xref:microsoft.quantum.lang-ref.double)

Hoek over de opgegeven multi-Qubit Pauli-operator waarmee het doel register moet worden gedraaid.


### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Meld u aan om de gegeven draaiing toe te passen op.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

