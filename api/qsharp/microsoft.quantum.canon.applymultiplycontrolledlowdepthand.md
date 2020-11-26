---
uid: Microsoft.Quantum.Canon.ApplyMultiplyControlledLowDepthAnd
title: Bewerking ApplyMultiplyControlledLowDepthAnd
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyMultiplyControlledLowDepthAnd
qsharp.summary: Implements a multiple-controlled Toffoli gate, assuming that target qubit is initialized 0.  The adjoint operation assumes that the target qubit will be reset to 0.  Requires a Rz depth of 1, while the number of helper qubits are exponential in the number of qubits.
ms.openlocfilehash: 1aeab429bd6304c621e0d5225b43a76eab607c84
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209193"
---
# <a name="applymultiplycontrolledlowdepthand-operation"></a>Bewerking ApplyMultiplyControlledLowDepthAnd

Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementeert een multi-beheerde Toffoli-Gate, ervan uitgaande dat de doel-Qubit 0 is geïnitialiseerd.  Bij de bewerking adjoint wordt ervan uitgegaan dat de doel-Qubit opnieuw wordt ingesteld op 0.  Vereist een RZ diepte van 1, terwijl het aantal helper-qubits exponentieel is in het aantal qubits.

```qsharp
operation ApplyMultiplyControlledLowDepthAnd (controls : Qubit[], target : Qubit) : Unit is Adj
```


## <a name="input"></a>Invoer

### <a name="controls--qubit"></a>Besturings elementen: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubits beheren


### <a name="target--qubit"></a>doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)

Doel-Qubit



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

