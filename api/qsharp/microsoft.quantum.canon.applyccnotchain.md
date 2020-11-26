---
uid: Microsoft.Quantum.Canon.ApplyCCNOTChain
title: Bewerking ApplyCCNOTChain
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCCNOTChain
qsharp.summary: Implements a cascade of CCNOT gates controlled on corresponding bits of two qubit registers, acting on the next qubit of one of the registers. Starting from the qubits at position 0 in both registers as controls, CCNOT is applied to the qubit at position 1 of the target register, then controlled by the qubits at position 1 acting on the qubit at position 2 in the target register, etc., ending with an action on the target qubit in position `Length(nQubits)-1`.
ms.openlocfilehash: 275f31ea636d15eb0d78e5148e8af6b58d22729d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209652"
---
# <a name="applyccnotchain-operation"></a>Bewerking ApplyCCNOTChain

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Hiermee wordt een trapsgewijs aantal CCNOT-poorten geïmplementeerd dat wordt beheerd op overeenkomstige bits van twee Qubit-registers, op de volgende Qubit van een van de registers.
Vanaf de qubits op positie 0 in beide registers als besturings elementen, wordt CCNOT toegepast op de Qubit op positie 1 van het doel register en vervolgens beheerd door de qubits op positie 1 op de Qubit op positie 2 in het doel register, enzovoort, eindigend met een actie op de doel-Qubit op positie `Length(nQubits)-1` .

```qsharp
operation ApplyCCNOTChain (register : Qubit[], targets : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="register--qubit"></a>registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubit-REGI ster, alleen gebruikt voor besturings elementen.


### <a name="targets--qubit"></a>doelen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubit-REGI ster, gebruikt voor besturings elementen en als doel.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

Het REGI ster van de doel-Qubit moet één Qubit meer dan het andere REGI ster hebben.