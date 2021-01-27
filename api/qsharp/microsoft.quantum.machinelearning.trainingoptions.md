---
uid: Microsoft.Quantum.MachineLearning.TrainingOptions
title: Door de gebruiker gedefinieerd TrainingOptions-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: TrainingOptions
qsharp.summary: A collection of options to be used in training quantum classifiers.
ms.openlocfilehash: 762d6853910832c6d4cda522c0c5df706d1ed195
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842771"
---
# <a name="trainingoptions-user-defined-type"></a>Door de gebruiker gedefinieerd TrainingOptions-type

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Een verzameling opties die moeten worden gebruikt in de Quantum-classificaties voor de training.

```qsharp

newtype TrainingOptions = (LearningRate : Double, Tolerance : Double, MinibatchSize : Int, NMeasurements : Int, MaxEpochs : Int, MaxStalls : Int, StochasticRescaleFactor : Double, ScoringPeriod : Int, VerboseMessage : (String -> Unit));
```



## <a name="named-items"></a>Benoemde items

### <a name="learningrate--double"></a>Leer tempo valt: [dubbel](xref:microsoft.quantum.lang-ref.double)

Het leer tempo waarmee kleur overgangen moeten worden aangepast bij het bijwerken van model parameters tijdens de trainings stappen.
### <a name="tolerance--double"></a>Tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)

De aanpassings tolerantie die moet worden gebruikt bij het voorbereiden van voor beelden als Quantum status.
### <a name="minibatchsize--int"></a>MinibatchSize: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal voor beelden dat moet worden gebruikt in de minibatch van de training.
### <a name="nmeasurements--int"></a>NMeasurements: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal keer dat elk classificatie resultaat moet worden gemeten om de classificatie waarschijnlijkheid te schatten.
### <a name="maxepochs--int"></a>MaxEpochs: [int](xref:microsoft.quantum.lang-ref.int)

Het maximum aantal epoches voor het trainen van elk model voor.
### <a name="maxstalls--int"></a>MaxStalls: [int](xref:microsoft.quantum.lang-ref.int)

Het maximum aantal keren dat een trainings-epoche mag worden gestopt (ongeveer nul kleur overgang) voordat er een fout optreedt.
### <a name="stochasticrescalefactor--double"></a>StochasticRescaleFactor: [dubbel](xref:microsoft.quantum.lang-ref.double)

De hoeveelheid voor het herschalen van gereduceerde modellen door voordat een update opnieuw wordt uitgevoerd.
### <a name="scoringperiod--int"></a>ScoringPeriod: [int](xref:microsoft.quantum.lang-ref.int)

Het aantal verloop stappen dat moet worden genomen tussen score punten.
Stel de beste nauw keurigheid in op 1.
### <a name="verbosemessage--string---unit"></a>VerboseMessage: [teken reeks](xref:microsoft.quantum.lang-ref.string) -> [eenheid](xref:microsoft.quantum.lang-ref.unit)

Een functie die kan worden gebruikt om uitgebreide feedback te geven.

## <a name="remarks"></a>Opmerkingen

Deze UDT mag niet direct worden gemaakt, maar moet in plaats daarvan worden opgegeven door @"microsoft.quantum.machinelearning.defaulttrainingoptions" de `w/` operator aan te roepen en vervolgens te gebruiken om verschillende standaard waarden te overschrijven.

Als u bijvoorbeeld 100.000 metingen en Maxi maal 8 trainings-epochen wilt gebruiken:

```qsharp
let options = DefaultTrainingOptions()
              w/ NMeasurements <- 100000
              w/ MaxEpochs <- 8;
```

## <a name="references"></a>Verwijzingen

- [arXiv:1804.00633](https://arxiv.org/abs/1804.00633)