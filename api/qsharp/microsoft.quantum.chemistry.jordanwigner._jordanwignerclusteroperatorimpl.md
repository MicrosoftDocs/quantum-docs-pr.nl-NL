---
uid: Microsoft.Quantum.Chemistry.JordanWigner._JordanWignerClusterOperatorImpl
title: _JordanWignerClusterOperatorImpl bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: _JordanWignerClusterOperatorImpl
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.

  See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.
ms.openlocfilehash: 9507558ebe73bce87d9089aad22b94c1d9d579d0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703454"
---
# <a name="_jordanwignerclusteroperatorimpl-operation"></a>_JordanWignerClusterOperatorImpl bewerking

Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)

Pakket [](https://nuget.org/packages/)


Dit object vertegenwoordigt een dynamische generator als een set simulatieve Gates en een uitbrei ding in de JordanWigner basis.

Zie [model lering van dynamische Generator](../libraries/data-structures#dynamical-generator-modeling) voor meer informatie.

```qsharp
operation _JordanWignerClusterOperatorImpl (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a>Invoer

### <a name="generatorindex--generatorindex"></a>generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Een generator index die wordt weer gegeven als unitary-ontwikkeling in de JordanWigner.


### <a name="stepsize--double"></a>stepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)

Dummy variabele die overeenkomt met de hand tekening van simulatie algoritmen.


### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Registratie van de actie op basis van tijd-ontwikkelings operator.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

