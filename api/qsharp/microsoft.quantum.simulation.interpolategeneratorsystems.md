---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystems
title: De functie InterpolateGeneratorSystems
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystems
qsharp.summary: Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.
ms.openlocfilehash: ee47637996313fe1b77c76f00b08417dac956247
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230579"
---
# <a name="interpolategeneratorsystems-function"></a>De functie InterpolateGeneratorSystems

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Retourneert een waarde `TimeDependentGeneratorSystem` die de lineaire interpolatie tussen twee `GeneratorSystem` s aangeeft.

```qsharp
function InterpolateGeneratorSystems (generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
```


## <a name="input"></a>Invoer

### <a name="generatorsystemstart--generatorsystem"></a>generatorSystemStart: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Het begin `GeneratorSystem` .


### <a name="generatorsystemend--generatorsystem"></a>generatorSystemEnd: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Het einde `GeneratorSystem` .



## <a name="output--timedependentgeneratorsystem"></a>Uitvoer: [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)

Een `TimeDependentGeneratorSystem` vertegenwoordigt een systeem dat de som is van de invoer Generator systemen, waarbij gewicht $ (1-s) $ op `generatorSystemStart` en gewicht $s $ is ingeschakeld `generatorSystemEnd` .

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. simulatie. GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
- [Micro soft. Quantum. simulatie. TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)