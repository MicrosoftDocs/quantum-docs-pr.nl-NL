---
uid: Microsoft.Quantum.Simulation.InterpolatedEvolution
title: De functie InterpolatedEvolution
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolatedEvolution
qsharp.summary: Interpolates between two generators with a uniform schedule, returning an operation that applies simulated evolution under the resulting time-dependent generator to a qubit register.
ms.openlocfilehash: 2ad907c02a2412dd4bf95630f401b5f1db5c8a08
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96225105"
---
# <a name="interpolatedevolution-function"></a>De functie InterpolatedEvolution

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Interpoleert twee generatoren met een uniform schema, waarbij een bewerking wordt geretourneerd waarmee gesimuleerde evoluties worden toegepast onder de resulterende tijd afhankelijke Generator naar een Qubit-REGI ster.

```qsharp
function InterpolatedEvolution (interpolationTime : Double, evolutionGeneratorStart : Microsoft.Quantum.Simulation.EvolutionGenerator, evolutionGeneratorEnd : Microsoft.Quantum.Simulation.EvolutionGenerator, timeDependentSimulationAlgorithm : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a>Invoer

### <a name="interpolationtime--double"></a>interpolationTime: [dubbel](xref:microsoft.quantum.lang-ref.double)

Tijd waarop de interpolatie moet worden uitgevoerd.


### <a name="evolutiongeneratorstart--evolutiongenerator"></a>evolutionGeneratorStart: [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

Initiële generator voor het simuleren van de ontwikkeling onder.


### <a name="evolutiongeneratorend--evolutiongenerator"></a>evolutionGeneratorEnd: [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)

Definitieve generator voor het simuleren van de ontwikkeling onder.


### <a name="timedependentsimulationalgorithm--timedependentsimulationalgorithm"></a>timeDependentSimulationAlgorithm: [timeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)

Een tijdgebonden simulatie algoritme dat wordt gebruikt voor het simuleren van de evolutie tijdens het uniforme interpolatie schema.



## <a name="output--qubit--unit--is-adj--ctl"></a>Output: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL



## <a name="remarks"></a>Opmerkingen

Als de interpolatie tijd is gekozen om te voldoen aan de Adiabatic-voor waarden, retourneert deze functie een bewerking die Adiabatic-status voorbereiding uitvoert voor de laatste dynamische generator.