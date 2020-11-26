---
uid: Microsoft.Quantum.MachineLearning.NQubitsRequired
title: De functie NQubitsRequired
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: NQubitsRequired
qsharp.summary: Returns the number of qubits required to apply a given sequential classifier.
ms.openlocfilehash: e910edb9bf432e6acb5c349ee6b9d65797aaaba7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211658"
---
# <a name="nqubitsrequired-function"></a>De functie NQubitsRequired

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Retourneert het aantal qubits dat vereist is om een bepaalde sequentiële classificatie toe te passen.

```qsharp
function NQubitsRequired (model : Microsoft.Quantum.MachineLearning.SequentialModel) : Int
```


## <a name="input"></a>Invoer

### <a name="model--sequentialmodel"></a>model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)





## <a name="output--int"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int)

De minimale grootte van een REGI ster waarop de sequentiële classificatie kan worden toegepast.