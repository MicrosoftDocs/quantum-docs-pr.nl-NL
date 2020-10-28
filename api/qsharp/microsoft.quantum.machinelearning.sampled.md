---
uid: Microsoft.Quantum.MachineLearning.Sampled
title: Voorbeeld functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: Sampled
qsharp.summary: Samples a given array, using the given schedule.
ms.openlocfilehash: 9f9f91bc50861c5b31a76e28050189d13efda71e
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707975"
---
# <a name="sampled-function"></a>Voorbeeld functie

Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)

Pakket [](https://nuget.org/packages/)


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

