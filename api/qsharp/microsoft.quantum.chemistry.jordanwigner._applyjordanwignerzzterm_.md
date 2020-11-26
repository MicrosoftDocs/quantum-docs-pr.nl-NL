---
uid: Microsoft.Quantum.Chemistry.JordanWigner._ApplyJordanWignerZZTerm_
title: Bewerking _ApplyJordanWignerZZTerm_
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _ApplyJordanWignerZZTerm_
qsharp.summary: Applies time-evolution by a ZZ term described by a `GeneratorIndex`.
ms.openlocfilehash: 346dc18d3d70899eab0800a3087703aa42055a04
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96215857"
---
# <a name="_applyjordanwignerzzterm_-operation"></a>Bewerking _ApplyJordanWignerZZTerm_

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)


Past tijd-evolutie toe op basis van een ZZ-term die wordt beschreven door een `GeneratorIndex` .

```qsharp
operation _ApplyJordanWignerZZTerm_ (term : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="term--generatorindex"></a>term: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

`GeneratorIndex` vertegenwoordigt een ZZ-term.


### <a name="stepsize--double"></a>stepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)

Duur van tijd-ontwikkeling.


### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubits van Hamiltonian.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

