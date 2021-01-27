---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Voorbeeld functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: 5dd599246847718f4f0411715585cb416595db9d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854954"
---
# <a name="sampled-function"></a>Voorbeeld functie

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)


Voor beelden van een bepaalde matrix, met behulp van het opgegeven schema.

```qsharp
function Sampled<'T> (schedule : Microsoft.Quantum.MachineLearning.SamplingSchedule, values : 'T[]) : 'T[]
```


## <a name="input"></a>Invoer

### <a name="schedule--samplingschedule"></a>planning: [SamplingSchedule](xref:Microsoft.Quantum.MachineLearning.SamplingSchedule)

Een schema dat moet worden gebruikt in sampling waarden.


### <a name="values--t"></a>waarden: ' []

Een matrix met waarden waarvan u een steek proef wilt maken.



## <a name="output--t"></a>Uitvoer: ' []

Een matrix met elementen van waarden, volgens het opgegeven schema.

## <a name="type-parameters"></a>Type parameters

### <a name="t"></a>T

