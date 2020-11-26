---
uid: Microsoft.Quantum.Canon.ApplyPauliFromBitString
title: Bewerking ApplyPauliFromBitString
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauliFromBitString
qsharp.summary: Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.
ms.openlocfilehash: cf4c99ec5134fac788cdd4c8a057258790152a82
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209057"
---
# <a name="applypaulifrombitstring-operation"></a>Bewerking ApplyPauliFromBitString

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Past een Pauli-operator op elke qubit in een matrix toe als de overeenkomstige bit van een Boole-matrix overeenkomt met een gegeven invoer.

```qsharp
operation ApplyPauliFromBitString (pauli : Pauli, bitApply : Bool, bits : Bool[], qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="pauli--pauli"></a>Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

De operator Pauli die moet worden toegepast op `qubits[idx]` WHERE `bitsApply == bits[idx]`


### <a name="bitapply--bool"></a>bitApply: [BOOL](xref:microsoft.quantum.lang-ref.bool)

Pauli Toep assen als bit deze waarde is


### <a name="bits--bool"></a>bits: [BOOL](xref:microsoft.quantum.lang-ref.bool)[]

Booleaanse registratie voor het opgeven van de bijbehorende Qubit in `qubits` moet worden gebruikt


### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Quantum registratie voor selectief Toep assen van de opgegeven Pauli-operator



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="remarks"></a>Opmerkingen

De Boole-matrix en het Quantum register moeten even lang zijn.