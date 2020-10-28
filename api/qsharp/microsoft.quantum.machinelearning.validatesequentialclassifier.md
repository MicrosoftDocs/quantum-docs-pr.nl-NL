---
uid: Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier
title: Bewerking ValidateSequentialClassifier
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidateSequentialClassifier
qsharp.summary: Validates a given sequential classifier against a given set of pre-labeled samples.
ms.openlocfilehash: 802f1045ea4086bd371d68018a481182cb75b209
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706828"
---
# <a name="validatesequentialclassifier-operation"></a>Bewerking ValidateSequentialClassifier

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket [](https://nuget.org/packages/)


Hiermee wordt een bepaalde sequentiële classificatie gevalideerd op basis van een bepaalde set vooraf gelabelde voor beelden.

```qsharp
operation ValidateSequentialClassifier (model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Microsoft.Quantum.MachineLearning.LabeledSample[], tolerance : Double, nMeasurements : Int, validationSchedule : Microsoft.Quantum.MachineLearning.SamplingSchedule) : Microsoft.Quantum.MachineLearning.ValidationResults
```


## <a name="input"></a>Invoer

### <a name="model--sequentialmodel"></a>model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Het sequentiële model dat moet worden gevalideerd.


### <a name="samples--labeledsample"></a>voor beelden: [LabeledSample](xref:Microsoft.Quantum.MachineLearning.LabeledSample)[]

De voor beelden die moeten worden gebruikt om het opgegeven model te valideren.


### <a name="tolerance--double"></a>tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)

De benaderings tolerantie die moet worden gebruikt voor het coderen van elk voor beeld als invoer voor de sequentiële classificatie.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal metingen dat moet worden gebruikt bij het classificeren van elk voor beeld.


### <a name="validationschedule--samplingschedule"></a>validationSchedule: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Het schema waarmee steek proeven worden getekend vanuit de validatieset.



## <a name="output--validationresults"></a>Uitvoer: [ValidationResults](xref:Microsoft.Quantum.MachineLearning.ValidationResults)

De resultaten van de opgegeven validatie.