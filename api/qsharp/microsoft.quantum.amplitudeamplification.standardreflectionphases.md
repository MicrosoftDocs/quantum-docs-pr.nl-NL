---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: De functie StandardReflectionPhases
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: c189b34b641989ab458986fb3f2872759b949be5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707680"
---
# <a name="standardreflectionphases-function"></a>De functie StandardReflectionPhases

Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pakket [](https://nuget.org/packages/)


Berekent gedeeltelijke reflectie fasen voor standaard amplitude versterking.

```qsharp
function StandardReflectionPhases (nIterations : Int) : Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases
```


## <a name="input"></a>Invoer

### <a name="niterations--int"></a>nIterations: [int](xref:microsoft.quantum.lang-ref.int)

Aantal amplitude versterkings herhalingen waarvoor gedeeltelijke reflectie fasen worden gegenereerd.



## <a name="output--reflectionphases"></a>Uitvoer: [ReflectionPhases](xref:Microsoft.Quantum.AmplitudeAmplification.ReflectionPhases)

Een bewerking waarmee fasen worden geïmplementeerd die zijn opgegeven als gedeeltelijke reflecties

## <a name="remarks"></a>Opmerkingen

Alle fasen zijn $ \pi $, met uitzonde ring van de eerste reflectie over de begin status en de laatste reflectie over de doel status, die $0 $ zijn.