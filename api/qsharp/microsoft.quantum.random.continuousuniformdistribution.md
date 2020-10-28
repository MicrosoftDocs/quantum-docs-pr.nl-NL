---
uid: Microsoft.Quantum.Random.ContinuousUniformDistribution
title: De functie ContinuousUniformDistribution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: ContinuousUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive interval.
ms.openlocfilehash: 74300efb10ba7b5aa006f0b1b6aafde0da840f00
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701235"
---
# <a name="continuousuniformdistribution-function"></a>De functie ContinuousUniformDistribution

Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)

Pakket [](https://nuget.org/packages/)


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