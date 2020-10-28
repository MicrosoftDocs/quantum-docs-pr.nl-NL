---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerPQandPQQRTerm_
title: Bewerking _ApplyJordanWignerPQandPQQRTerm_
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerPQandPQQRTerm_
qsharp.summary: Applies time-evolution by a PQ or PQQR term described by a `GeneratorIndex`.
ms.openlocfilehash: a2a74ddeb7ecefaf4aa21374302d2709ee676e5d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703533"
---
# <a name="_applyjordanwignerpqandpqqrterm_-operation"></a>Bewerking _ApplyJordanWignerPQandPQQRTerm_

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pakket [](https://nuget.org/packages/)


Past tijd-evolutie toe met een PQ-of PQQR-term die wordt beschreven door een `GeneratorIndex` .

```qsharp
operation _ApplyJordanWignerPQandPQQRTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="term--generatorindex"></a>term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` een PQ-of PQQR-term vertegenwoordigt.


### <a name="stepsize--double"></a>stepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)

Duur van tijd-ontwikkeling.


### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubits van Hamiltonian.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

