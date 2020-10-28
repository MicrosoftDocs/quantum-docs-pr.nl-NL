---
uid: Microsoft.Quantum.Random.DiscreteUniformDistribution
title: De functie DiscreteUniformDistribution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Random
qsharp.name: DiscreteUniformDistribution
qsharp.summary: Returns a uniform distribution over a given inclusive range.
ms.openlocfilehash: 5e93c66d891d9b6aec548c0cf266df35e6090c92
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706725"
---
# <a name="discreteuniformdistribution-function"></a>De functie DiscreteUniformDistribution

Naam ruimte: [micro soft. Quantum. wille keurig](xref:Microsoft.Quantum.Random)

Pakket [](https://nuget.org/packages/)


Retourneert een uniforme distributie over een opgegeven inclusief bereik.

```qsharp
function DiscreteUniformDistribution (min : Int, max : Int) : Microsoft.Quantum.Random.DiscreteDistribution
```


## <a name="input"></a>Invoer

### <a name="min--int"></a>min: [int](xref:microsoft.quantum.lang-ref.int)

Het kleinste gehele getal dat moet worden getekend.


### <a name="max--int"></a>Max.: [int](xref:microsoft.quantum.lang-ref.int)

Het grootste gehele getal dat moet worden getekend.



## <a name="output--discretedistribution"></a>Uitvoer: [DiscreteDistribution](xref:Microsoft.Quantum.Random.DiscreteDistribution)

Een distributie waarvan de wille keurige variates gehele getallen in het inclusieve bereik zijn van `min` tot `max` met een uniforme kans.

## <a name="remarks"></a>Opmerkingen

Mislukt als `max <= min` .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. DrawRandomDouble](xref:Microsoft.Quantum.DrawRandomDouble)