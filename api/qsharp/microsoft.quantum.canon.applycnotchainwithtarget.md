---
uid: Microsoft.Quantum.Canon.ApplyCNOTChainWithTarget
title: Bewerking ApplyCNOTChainWithTarget
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChainWithTarget
qsharp.summary: Computes the parity of an array of qubits into a target qubit.
ms.openlocfilehash: 8ec85ce5805b3bbd1e1f7c739f27de3a861bc79e
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219104"
---
# <a name="applycnotchainwithtarget-operation"></a>Bewerking ApplyCNOTChainWithTarget

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt de pariteit van een matrix met qubits berekend in een doel-Qubit.

```qsharp
operation ApplyCNOTChainWithTarget (qubits : Qubit[], targetQubit : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a>Beschrijving

Als de matrix in eerste instantie de status $ \ket{q_0} \ket{q_1} \cdots \ket{q_ {\Text{target}}} $ heeft, wordt de uiteindelijke status gegeven door $ \ket{q_0} \ket{q_1 \oplus q_0} \cdots \ket{q_ {n-1} \oplus \cdots \oplus q_0 \oplus q_ {\Text{target}}} $.

## <a name="input"></a>Invoer

### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Matrix van qubits waarop de pariteit wordt berekend.


### <a name="targetqubit--qubit"></a>targetQubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Eind Qubit waarin de pariteit van qubits is XORed.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

De volgende zijn gelijkwaardig:

```qsharp
ApplyCNOTChainWithTarget(Most(qs), Last(qs));
```

en

```qsharp
ApplyCNOTChain(qs);
```