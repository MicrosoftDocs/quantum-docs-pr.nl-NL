---
uid: Microsoft.Quantum.MachineLearning.ApplySequentialClassifier
title: Bewerking ApplySequentialClassifier
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ApplySequentialClassifier
qsharp.summary: Given the structure and parameterization of a sequential classifier, applies the classifier to a register of qubits.
ms.openlocfilehash: fe1ca5717f18cc0816b96ddd29ce89c568571791
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212015"
---
# <a name="applysequentialclassifier-operation"></a>Bewerking ApplySequentialClassifier

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Op basis van de structuur en het parameterisering van een sequentiële classificatie wordt de classificatie toegepast op een REGI ster van qubits.

```qsharp
operation ApplySequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a>Invoer

### <a name="model--sequentialmodel"></a>model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)




### <a name="qubits--qubit"></a>qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]

Een doel registratie waarop de classificatie moet worden toegepast.



## <a name="output--unit"></a>Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)

