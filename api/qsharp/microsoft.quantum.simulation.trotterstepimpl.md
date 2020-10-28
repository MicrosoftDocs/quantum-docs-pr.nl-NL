---
uid: Microsoft.Quantum.Simulation.TrotterStepImpl
title: Bewerking TrotterStepImpl
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStepImpl
qsharp.summary: Implements time-evolution by a term contained in a `GeneratorSystem`.
ms.openlocfilehash: 1ddd7ab33df243d729b5b48cba393d976bfd3640
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709217"
---
# <a name="trotterstepimpl-operation"></a>Bewerking TrotterStepImpl

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket [](https://nuget.org/packages/)


Implementeert tijd ontwikkeling met een term die is opgenomen in een `GeneratorSystem` .

```qsharp
operation TrotterStepImpl (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, idx : Int, stepsize : Double, qubits : Qubit[]) : Unit
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

