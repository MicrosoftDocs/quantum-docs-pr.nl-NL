---
uid: Microsoft.Quantum.Canon.ApplyCNOTChainWithTarget
title: Bewerking ApplyCNOTChainWithTarget
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChainWithTarget
qsharp.summary: Computes the parity of an array of qubits into a target qubit.
ms.openlocfilehash: fd0a0f3e1db89946aec2c63f3cde7a021608eea5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705437"
---
# <a name="applycnotchainwithtarget-operation"></a>Bewerking ApplyCNOTChainWithTarget

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket [](https://nuget.org/packages/)


Hiermee wordt de pariteit van een matrix met qubits berekend in een doel-Qubit.

```qsharp
operation ApplyCNOTChainWithTarget (qubits : Qubit[], targetQubit : Qubit) : Unit
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