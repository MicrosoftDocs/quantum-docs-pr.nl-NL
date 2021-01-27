---
uid: Microsoft.Quantum.Intrinsic.ExpFrac
title: Bewerking ExpFrac
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ExpFrac
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.

  \begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: 6634caff164c841876fb53e79c3f93254a7d624c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849419"
---
# <a name="expfrac-operation"></a>Bewerking ExpFrac

Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Past de exponentiële waarde toe van een multi-Qubit Pauli-operator met een argument dat door een dyadic-fractie wordt gegeven.

\begin{align} e ^ {i \pi k [P_0 \otimes P_1 \cdots P_ {N-1}]/2 ^ N}, \end{align} waarbij $P _i $ het $i $ TH element van is `paulis` en waar $N = $ `Length(paulis)` .

```qsharp
operation ExpFrac (paulis : Pauli[], numerator : Int, power : Int, qubits : Qubit[]) : Unit is Adj + Ctl
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

