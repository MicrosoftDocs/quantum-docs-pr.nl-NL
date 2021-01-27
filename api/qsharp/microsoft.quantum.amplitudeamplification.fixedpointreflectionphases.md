---
uid: Microsoft.Quantum.AmplitudeAmplification.FixedPointReflectionPhases
title: De functie FixedPointReflectionPhases
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: FixedPointReflectionPhases
qsharp.summary: Computes partial reflection phases for fixed-point amplitude amplification.
ms.openlocfilehash: 2ded197801111c26d8a33f9c2363b46ca4b6c4b9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845845"
---
# <a name="fixedpointreflectionphases-function"></a>De functie FixedPointReflectionPhases

Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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

## <a name="references"></a>Verwijzingen

We gebruiken de fasen in ' amplitude versterking met een optimaal aantal Query's '

- [YoderLowChuang2014](https://arxiv.org/abs/1409.3305) Zie ook ' methodologie van samengestelde Quantum Gates '
- [LowYoderChuang2016](https://arxiv.org/abs/1603.03996) voor fasen in de `RotationPhases` indeling.