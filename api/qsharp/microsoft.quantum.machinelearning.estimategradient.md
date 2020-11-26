---
uid: Microsoft.Quantum.MachineLearning.EstimateGradient
title: Bewerking EstimateGradient
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: EstimateGradient
qsharp.summary: Estimates the training gradient for a sequential classifier at a particular model and for a given encoded input.
ms.openlocfilehash: 79f4abdf131509d4948a3c114e631118329f88d8
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211845"
---
# <a name="estimategradient-operation"></a>Bewerking EstimateGradient

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Maakt een schatting van de cursus verloop voor een sequentiële classificatie in een bepaald model en voor een gegeven gecodeerde invoer.

```qsharp
operation EstimateGradient (model : Microsoft.Quantum.MachineLearning.SequentialModel, encodedInput : Microsoft.Quantum.MachineLearning.StateGenerator, nMeasurements : Int) : Double[]
```


## <a name="input"></a>Invoer

### <a name="model--sequentialmodel"></a>model: [SequentialModel](xref:Microsoft.Quantum.MachineLearning.SequentialModel)

Het sequentiële model waarvan het verloop moet worden geschat.


### <a name="encodedinput--stategenerator"></a>encodedInput: [StateGenerator](xref:Microsoft.Quantum.MachineLearning.StateGenerator)

Een invoer van de sequentiële classificatie, gecodeerd in een status voorbereidings bewerking.


### <a name="nmeasurements--int"></a>nMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal metingen dat moet worden gebruikt bij het schatten van de kleur overgang.



## <a name="output--double"></a>Uitvoer: [dubbele](xref:microsoft.quantum.lang-ref.double)[]

Een schatting van de verloop tijd van de training bij de gegeven para meters voor invoer en model.

## <a name="remarks"></a>Opmerkingen

Deze bewerking maakt gebruik van een Hadamard-test en de para meter Shift-techniek om de kleur overgang te schatten.