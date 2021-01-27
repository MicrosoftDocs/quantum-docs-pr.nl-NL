---
uid: Microsoft.Quantum.MachineLearning.EstimateClassificationProbability
title: Bewerking EstimateClassificationProbability
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateClassificationProbability
qsharp.summary: Given a sample and a sequential classifier, estimates the classification probability for that sample by repeatedly measuring the output of the classifier on the given sample.
ms.openlocfilehash: c2b74bc55ad9005a8f52d05796e856f4f2fb62ba
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853943"
---
# <a name="estimateclassificationprobability-operation"></a>Bewerking EstimateClassificationProbability

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Op basis van een voor beeld en een sequentiële classificatie schat de classificatie waarschijnlijkheid van het voor beeld door de uitvoer van de classificatie op basis van het opgegeven voor beeld herhaaldelijk te meten.

```qsharp
operation EstimateClassificationProbability (tolerance : Double, model : Microsoft.Quantum.MachineLearning.SequentialModel, sample : Double[], nMeasurements : Int) : Double
```


## <a name="input"></a>Invoer

### <a name="tolerance--double"></a>tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)

De tolerantie voor het coderen van het voor beeld in een status voorbereidings bewerking.


### <a name="model--sequentialmodel"></a>model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Het sequentiële model dat moet worden gebruikt om de classificatie waarschijnlijkheid voor het opgegeven voor beeld te schatten.


### <a name="sample--double"></a>voor beeld: [dubbele](xref:microsoft.quantum.lang-ref.double)[]

De functie Vector voor het voor beeld dat moet worden geclassificeerd.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal metingen dat moet worden gebruikt bij het schatten van de classificatie waarschijnlijkheid.



## <a name="output--double"></a>Uitvoer: [dubbel](xref:microsoft.quantum.lang-ref.double)

Een schatting van de classificatie waarschijnlijkheid voor het gegeven voor beeld.