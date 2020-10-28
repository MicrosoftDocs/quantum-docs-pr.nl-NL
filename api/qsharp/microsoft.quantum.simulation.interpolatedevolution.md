---
uid: Microsoft.Quantum.Simulation.InterpolatedEvolution
title: De functie InterpolatedEvolution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolatedEvolution
qsharp.summary: Interpolates between two generators with a uniform schedule, returning an operation that applies simulated evolution under the resulting time-dependent generator to a qubit register.
ms.openlocfilehash: 18026b9872f6a3344a1e5c2122f55927975ccb59
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701732"
---
# <a name="interpolatedevolution-function"></a>De functie InterpolatedEvolution

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket [](https://nuget.org/packages/)


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



## <a name="output--qubit--unit-adj--ctl"></a>Output: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL



## <a name="remarks"></a>Opmerkingen

Als de interpolatie tijd is gekozen om te voldoen aan de Adiabatic-voor waarden, retourneert deze functie een bewerking die Adiabatic-status voorbereiding uitvoert voor de laatste dynamische generator.