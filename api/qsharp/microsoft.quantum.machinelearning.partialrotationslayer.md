---
uid: Microsoft.Quantum.MachineLearning.PartialRotationsLayer
title: De functie PartialRotationsLayer
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: PartialRotationsLayer
qsharp.summary: Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.
ms.openlocfilehash: e230df9b28c59e1d532d5b36adf90efa01f0f33e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852924"
---
# <a name="partialrotationslayer-function"></a>De functie PartialRotationsLayer

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Retourneert een matrix met enkelvoudige draaiing langs een bepaalde as, para meters door afzonderlijke model parameters.

```qsharp
function PartialRotationsLayer (idxsQubits : Int[], axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a>Invoer

### <a name="idxsqubits--int"></a>idxsQubits: [int](xref:microsoft.quantum.lang-ref.int)[]

Indexen voor de qubits die moeten worden gebruikt als de doelen voor elke draaiing.


### <a name="axis--pauli"></a>as: [Pauli](xref:microsoft.quantum.lang-ref.pauli)

De rotatieas voor elke draaiing in de opgegeven laag.



## <a name="output--controlledrotation"></a>Uitvoer: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]

Een matrix met beheerde rotaties over de opgegeven as, één op elk van de `nQubits` qubits.