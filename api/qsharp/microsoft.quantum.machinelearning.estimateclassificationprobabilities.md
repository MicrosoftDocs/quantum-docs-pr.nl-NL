---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbabilities
title: Bewerking EstimateClassificationProbabilities
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbabilities
qsharp.summary: Given a set of samples and a sequential classifier, estimates the classification probability for those samples by repeatedly measuring the output of the classifier on each sample.
ms.openlocfilehash: 2b7845d39256f718cc3e415207b8a47b24620bdb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701390"
---
# <a name="estimateclassificationprobabilities-operation"></a>Bewerking EstimateClassificationProbabilities

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket [](https://nuget.org/packages/)


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