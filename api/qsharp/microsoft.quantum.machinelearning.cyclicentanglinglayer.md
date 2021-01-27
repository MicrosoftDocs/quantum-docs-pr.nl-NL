---
uid: Microsoft.Quantum.MachineLearning.CyclicEntanglingLayer
title: De functie CyclicEntanglingLayer
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CyclicEntanglingLayer
qsharp.summary: Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.
ms.openlocfilehash: 5d0af0a60217b69dc7eb8ece8952f2a7f0c09280
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847388"
---
# <a name="cyclicentanglinglayer-function"></a>De functie CyclicEntanglingLayer

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Retourneert een matrix met op zichzelf staande rotaties langs een bepaalde as, geordend op cyclische basis in een REGI ster van qubits en para meters door afzonderlijke model parameters.

```qsharp
function CyclicEntanglingLayer (nQubits : Int, axis : Pauli, stride : Int) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>Invoer

### <a name="nqubits--int"></a>nQubits: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal qubits dat wordt verwerkt door de opgegeven laag.


### <a name="axis--pauli"></a>as: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

De rotatieas voor elke draaiing in de opgegeven laag.


### <a name="stride--int"></a>Stride: [int](xref:microsoft.quantum.lang-ref.int)

De schei ding tussen de doel-en besturings indexen voor elke draaiing.



## <a name="output--controlledrotation"></a>Uitvoer: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Een matrix van door Qubit beheerde rotaties die cyclisch zijn verdeeld over een REGI ster van `nQubits` qubits.

## <a name="example"></a>Voorbeeld

De volgende zijn gelijkwaardig:

```qsharp
let layer = CyclicEntanglingLayer(3, PauliX, 2);
let layer = [
    ControlledRotation((0, [2]), PauliX, 0),
    ControlledRotation((1, [0]), PauliX, 1),
    ControlledRotation((2, [1]), PauliX, 2)
];
```