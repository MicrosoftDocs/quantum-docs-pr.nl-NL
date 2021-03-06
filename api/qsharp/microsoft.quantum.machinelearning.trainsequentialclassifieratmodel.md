---
uid: Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel
title: Bewerking TrainSequentialClassifierAtModel
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainSequentialClassifierAtModel
qsharp.summary: Given the structure of a sequential classifier, trains the classifier on a given labeled training set, starting from a particular model.
ms.openlocfilehash: 4164c190cb19b6d3ea74d9803a77d2b19607279b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857162"
---
# <a name="trainsequentialclassifieratmodel-operation"></a>Bewerking TrainSequentialClassifierAtModel

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Gezien de structuur van een sequentiële classificatie, traint de classificatie op een bepaald gelabelde Trainingsset, beginnend bij een bepaald model.

```qsharp
operation TrainSequentialClassifierAtModel (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, trainingSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : (Microsoft.Quantum.MachineLearning.SequentialModel, Int)
```


## <a name="input"></a>Invoer

### <a name="model--sequentialmodel"></a>model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Het sequentiële model dat moet worden gebruikt als uitgangs punt voor training.


### <a name="samples--labeledsample"></a>voor beelden: [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]

Een set gelabelde trainings gegevens die worden gebruikt voor het uitvoeren van training.


### <a name="options--trainingoptions"></a>opties: [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)

De configuratie die moet worden gebruikt bij het trainen; Zie @"microsoft.quantum.machinelearning.trainingoptions" en @"microsoft.quantum.machinelearning.defaulttrainingoptions" voor meer informatie.


### <a name="trainingschedule--samplingschedule"></a>trainingSchedule: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Een steekproef schema dat moet worden gebruikt bij het selecteren van voor beelden uit de trainings gegevens tijdens de trainings stappen.


### <a name="validationschedule--samplingschedule"></a>validationSchedule: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Een steekproef schema dat moet worden gebruikt bij het selecteren van steek proeven uit de opleidings gegevens wanneer wordt geselecteerd welk begin punt heeft geresulteerd in de beste classificatie Score.



## <a name="output--sequentialmodelint"></a>Uitvoer: ([SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel),[int](xref:microsoft.quantum.lang-ref.int))

- Een parameterisering van de gegeven classificatie en een afwijking tussen de twee klassen, samen met het beste resultaat van elk van de opgegeven begin punten.
- Het aantal missers dat bij het beste classificatie model is waargenomen.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. MachineLearning. TrainSequentialClassifier](xref:Microsoft.Quantum.MachineLearning.TrainSequentialClassifier)
- [Micro soft. Quantum. MachineLearning. ValidateSequentialClassifier](xref:Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier)