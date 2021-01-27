---
uid: Microsoft.Quantum.AmplitudeAmplification.StandardReflectionPhases
title: De functie StandardReflectionPhases
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.AmplitudeAmplification
qsharp.name: StandardReflectionPhases
qsharp.summary: Computes partial reflection phases for standard amplitude amplification.
ms.openlocfilehash: 703b50d0186cd0f4eddb9a29fa3cffb2b746c8d6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843921"
---
# <a name="standardreflectionphases-function"></a>De functie StandardReflectionPhases

Naam ruimte: [micro soft. Quantum. AmplitudeAmplification](xref:Microsoft.Quantum.AmplitudeAmplification)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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