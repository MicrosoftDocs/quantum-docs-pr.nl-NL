---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbabilities
title: Bewerking EstimateClassificationProbabilities
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbabilities
qsharp.summary: Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.
ms.openlocfilehash: 1cd56f6a6483b00afb168f8d84301e73eae9af65
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211896"
---
# <a name="estimateclassificationprobabilities-operation"></a>Bewerking EstimateClassificationProbabilities

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Op basis van een reeks voor beelden en een sequentiële classificatie schat de classificatie waarschijnlijkheid van deze voor beelden door herhaaldelijk de uitvoer van de classificatie voor elk voor beeld te meten.

```qsharp
operation EstimateClassificationProbabilities (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, samples : Double[][], nMeasurements : Int) : Double[]
```


## <a name="input"></a>Invoer

### <a name="tolerance--double"></a>tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)

De tolerantie voor het coderen van het voor beeld in een status voorbereidings bewerking.


### <a name="model--sequentialmodel"></a>model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Het sequentiële model dat moet worden gebruikt om de classificatie kansen voor de opgegeven steek proeven te schatten.


### <a name="samples--double"></a>voor beelden: [Double](xref:microsoft.quantum.lang-ref.double)[] []

Een matrix met functie vectoren voor elk voor beeld dat moet worden geclassificeerd.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal metingen dat moet worden gebruikt bij het schatten van de classificatie waarschijnlijkheid.



## <a name="output--double"></a>Uitvoer: [dubbele](xref:microsoft.quantum.lang-ref.double)[]

Een matrix met schattingen van de classificatie waarschijnlijkheid van elk gegeven voor beeld.