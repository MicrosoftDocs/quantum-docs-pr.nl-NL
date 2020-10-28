---
uid: Microsoft.Quantum.MachineLearning.TrainSequentialClassifier
title: Bewerking TrainSequentialClassifier
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainSequentialClassifier
qsharp.summary: Given the structure of a sequential classifier, trains the classifier on a given labeled training set.
ms.openlocfilehash: 12c4df59941b682d9de798e6585b59d1c34924dc
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702039"
---
# <a name="trainsequentialclassifier-operation"></a>Bewerking TrainSequentialClassifier

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket [](https://nuget.org/packages/)


Gezien de structuur van een sequentiële classificatie, traint de classificatie op een bepaald gelabelde opleidingsset.

```qsharp
operation TrainSequentialClassifier (models : Microsoft.Quantum.MachineLearning.SequentialModel[], samples : Microsoft.Quantum.MachineLearning.LabeledSample[], options : Microsoft.Quantum.MachineLearning.TrainingOptions, trainingSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : (Microsoft.Quantum.MachineLearning.SequentialModel, Int)
```


## <a name="input"></a>Invoer

### <a name="models--sequentialmodel"></a>modellen: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)[]

Een matrix van modellen die moeten worden gebruikt als uitgangs punt tijdens de training.


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

- [Micro soft. Quantum. MachineLearning. TrainSequentialClassifierAtModel](xref:Microsoft.Quantum.MachineLearning.TrainSequentialClassifierAtModel)
- [Micro soft. Quantum. MachineLearning. ValidateSequentialClassifier](xref:Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier)