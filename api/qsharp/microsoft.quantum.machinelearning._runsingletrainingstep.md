---
uid: Microsoft.Quantum.MachineLearning._RunSingleTrainingStep
title: _RunSingleTrainingStep bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: _RunSingleTrainingStep
qsharp.summary: attempts a single parameter update in the direction of mini batch gradient
ms.openlocfilehash: 2ee6dbbf26e8514ad59d156da12e0bcaca4ad7ae
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96212100"
---
# <a name="_runsingletrainingstep-operation"></a>_RunSingleTrainingStep bewerking

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


poging tot het bijwerken van één para meter in de richting van de mini maal batch verloop

```qsharp
operation _RunSingleTrainingStep (miniBatch : (Microsoft.Quantum.MachineLearning.LabeledSample, Microsoft.Quantum.MachineLearning.StateGenerator)[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, model : Microsoft.Quantum.MachineLearning.SequentialModel) : (Double, Microsoft.Quantum.MachineLearning.SequentialModel)
```


## <a name="input"></a>Invoer

### <a name="minibatch--labeledsamplestategenerator"></a>miniBatch: ([LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample),[StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)) []

container met gelabelde voor beelden in de batch


### <a name="options--trainingoptions"></a>opties: [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)




### <a name="model--sequentialmodel"></a>model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)





## <a name="output--doublesequentialmodel"></a>Uitvoer: ([Double](xref:microsoft.quantum.lang-ref.double),[SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel))

(hulp programma, (nieuwe) para meters)-paar