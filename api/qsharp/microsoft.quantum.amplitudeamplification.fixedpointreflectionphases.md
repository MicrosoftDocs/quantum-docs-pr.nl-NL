---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: De functie FixedPointReflectionPhases
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 6ab2a8c6cb0b390f96aa13ece5d5b89c196a6107
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707734"
---
# <a name="fixedpointreflectionphases-function"></a>De functie FixedPointReflectionPhases

Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pakket [](https://nuget.org/packages/)


Berekent gedeeltelijke reflectie fasen voor een amplitude versterking met een vaste komma.

```qsharp
function FixedPointReflectionPhases (nQueries : Int, successMin : Double) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a>Invoer

### <a name="nqueries--int"></a>nQueries: [int](xref:microsoft.quantum.lang-ref.int)

Aantal query's naar de status voorbereiding Oracle. Moet een oneven geheel getal zijn.


### <a name="successmin--double"></a>successMin: [dubbel](xref:microsoft.quantum.lang-ref.double)

Doel minimale succes volle kans.



## <a name="output--reflectionphases"></a>Uitvoer: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Matrix van fasen die kunnen worden gebruikt in de implementatie van een Quantum ring-algoritme met een vaste punt.

## <a name="references"></a>Naslaginformatie

We gebruiken de fasen in ' amplitude versterking met een optimaal aantal Query's '

- [YoderLowChuang2014](https://arxiv.org/abs/1409.3305) Zie ook ' methodologie van samengestelde Quantum Gates '
- [LowYoderChuang2016](https://arxiv.org/abs/1603.03996) voor fasen in de `RotationPhases` indeling.