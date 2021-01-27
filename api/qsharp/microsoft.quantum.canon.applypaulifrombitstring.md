---
uid: Microsoft.Quantum.Canon.ApplyPauliFromBitString
title: Bewerking ApplyPauliFromBitString
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyPauliFromBitString
qsharp.summary: Applies a Pauli operator on each qubit in an array if the corresponding bit of a Boolean array matches a given input.
ms.openlocfilehash: e0edd8420127339116e525421ba23e246dcf0a45
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841580"
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