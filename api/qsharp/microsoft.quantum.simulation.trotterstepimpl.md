---
uid: Microsoft.Quantum.Simulation.TrotterStepImpl
title: Bewerking TrotterStepImpl
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStepImpl
qsharp.summary: Implements time-evolution by a term contained in a `GeneratorSystem`.
ms.openlocfilehash: 33dc922cd5a60590a1306369fb99615fc6575b22
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856735"
---
# <a name="trotterstepimpl-operation"></a>Bewerking TrotterStepImpl

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Implementeert tijd ontwikkeling met een term die is opgenomen in een `GeneratorSystem` .

```qsharp
operation TrotterStepImpl (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, idx : Int, stepsize : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="evolutiongenerator--evolutiongenerator"></a>evolutionGenerator: [evolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

Een volledige beschrijving van het systeem dat moet worden gesimuleerd.


### <a name="idx--int"></a>idx: [int](xref:microsoft.quantum.lang-ref.int)

Gehele index naar een term in het beschreven systeem.


### <a name="stepsize--double"></a>stepsize: [dubbel](xref:microsoft.quantum.lang-ref.double)

Vermenigvuldiger met de duur van tijd-ontwikkeling per termijn die is geïndexeerd door `idx` .


### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Qubits heeft gehandeld op basis van simulatie.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

