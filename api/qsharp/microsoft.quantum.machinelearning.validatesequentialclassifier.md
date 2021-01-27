---
uid: Microsoft.Quantum.MachineLearning.ValidateSequentialClassifier
title: Bewerking ValidateSequentialClassifier
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: ValidateSequentialClassifier
qsharp.summary: Validates a given sequential classifier against a given set of pre-labeled samples.
ms.openlocfilehash: c100c5786b18996ce13067f1c4618cf0189578f5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848983"
---
# <a name="validatesequentialclassifier-operation"></a>Bewerking ValidateSequentialClassifier

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


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