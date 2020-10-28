---
uid: Microsoft.Quantum.Intrinsic.ExpFrac
title: Bewerking ExpFrac
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ExpFrac
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.

  \begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: d11912a272387b087098f59e7ac071534b01c054
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702117"
---
# <a name="expfrac-operation"></a>Bewerking ExpFrac

Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)

Pakket [](https://nuget.org/packages/)


Past de exponentiële waarde toe van een multi-Qubit Pauli-operator met een argument dat door een dyadic-fractie wordt gegeven.

\begin{align} e ^ {i \pi k [P_0 \otimes P_1 \cdots P_ {N-1}]/2 ^ N}, \end{align} waarbij $P _i $ het $i $ TH element van is `paulis` en waar $N = $ `Length(paulis)` .

```qsharp
operation ExpFrac (paulis : Pauli[], numerator : Int, power : Int, qubits : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="paulis--pauli"></a>PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]

Matrix van Pauli-waarden met één Qubit die de tensor-product factoren op elke qubit aangeven.


### <a name="numerator--int"></a>teller: [int](xref:microsoft.quantum.lang-ref.int)

Teller ($k $) in de dyadic-weer gave van de hoek waarmee het Qubit-REGI ster moet worden gedraaid.


### <a name="power--int"></a>energie: [int](xref:microsoft.quantum.lang-ref.int)

Kracht van twee ($n $) waarmee de noemer wordt aangegeven van de hoek waarmee het Qubit-REGI ster moet worden gedraaid.


### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Meld u aan om de gegeven draaiing toe te passen op.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

