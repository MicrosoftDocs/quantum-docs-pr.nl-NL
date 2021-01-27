---
uid: Microsoft.Quantum.MachineLearning.DefaultTrainingOptions
title: De functie DefaultTrainingOptions
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: DefaultTrainingOptions
qsharp.summary: Returns a default set of options for training classifiers.
ms.openlocfilehash: 474683ce5b9ec22bec686fb29d87728afe24d23a
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98855996"
---
# <a name="defaulttrainingoptions-function"></a>De functie DefaultTrainingOptions

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Retourneert een standaardset opties voor opleidings classificaties.

```qsharp
function DefaultTrainingOptions () : Microsoft.Quantum.MachineLearning.TrainingOptions
```


## <a name="output--trainingoptions"></a>Uitvoer: [TrainingOptions](xref:Microsoft.Quantum.MachineLearning.TrainingOptions)

Een redelijk aantal standaard opleidings opties voor het gebruik van classificaties voor trainingen.

## <a name="example"></a>Voorbeeld

Als u de standaard opties wilt gebruiken, maar met extra metingen, gebruikt u de `w/` operator:

```qsharp
let options = DefaultTrainingOptions()
    w/ NMeasurements <- 1000000;
```