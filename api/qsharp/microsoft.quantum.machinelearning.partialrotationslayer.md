---
uid: Microsoft.Quantum.MachineLearning.PartialRotationsLayer
title: De functie PartialRotationsLayer
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: PartialRotationsLayer
qsharp.summary: Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.
ms.openlocfilehash: ade0640b07f633982e98d5d02239fa205909bcce
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96196239"
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