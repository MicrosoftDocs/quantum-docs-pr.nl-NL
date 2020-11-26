---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: De functie ContinuousUniformDistribution
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: a3911fe9962ce18daa239de0272c53d83344134a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96193077"
---
# <a name="continuousuniformdistribution-function"></a>De functie ContinuousUniformDistribution

Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)

Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)


Retourneert een uniforme distributie over een opgegeven inclusief interval.

```qsharp
function ContinuousUniformDistribution (min : Double, max : Double) : Microsoft.Quantum.Random.ContinuousDistribution
```


## <a name="input"></a>Invoer

### <a name="min--double"></a>min: [dubbele](xref:microsoft.quantum.lang-ref.double)

Het kleinste reële getal dat moet worden getekend.


### <a name="max--double"></a>maximum: [Double](xref:microsoft.quantum.lang-ref.double)

Het grootste reële getal dat moet worden getekend.



## <a name="output--continuousdistribution"></a>Uitvoer: [ContinuousDistribution](xref:Microsoft.Quantum.Random.ContinuousDistribution)

Een distributie waarvan de wille keurige variates reële getallen in het inclusieve interval zijn, van `min` tot `max` met een uniforme kans.

## <a name="remarks"></a>Opmerkingen

Mislukt als `max <= min` .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. DrawRandomDouble](xref:Microsoft.Quantum.DrawRandomDouble)