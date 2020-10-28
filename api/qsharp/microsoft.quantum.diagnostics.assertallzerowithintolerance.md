---
uid: Microsoft.Quantum.Diagnostics.AssertAllZeroWithinTolerance
title: Bewerking AssertAllZeroWithinTolerance
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertAllZeroWithinTolerance
qsharp.summary: Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.
ms.openlocfilehash: 5e401904086323fabef7914d34463f50e4c38862
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702783"
---
# <a name="assertallzerowithintolerance-operation"></a>Bewerking AssertAllZeroWithinTolerance

Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)

Pakket [](https://nuget.org/packages/)


De bevestiging dat de opgegeven qubits zich in $ \ket $-status bevindt, {0} tot een gegeven tolerantie.

```qsharp
operation AssertAllZeroWithinTolerance (qubits : Qubit[], tolerance : Double) : Unit
```


## <a name="input"></a>Invoer

### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubits die zijn bewering over $ \ket $- {0} status.


### <a name="tolerance--double"></a>tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)

Nauw keurigheid waarmee de status moet worden in $ \ket {0} $ State



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)



## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. Diagnostics. AssertQubitWithinTolerance](xref:Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance)