---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorSystem
title: De functie MultiplyGeneratorSystem
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorSystem
qsharp.summary: Multiplies the coefficient of all terms in a `GeneratorSystem`.
ms.openlocfilehash: 1d28de99dab3f7aca4bf3706fe98f5ef7c5286a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706685"
---
# <a name="multiplygeneratorsystem-function"></a>De functie MultiplyGeneratorSystem

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket [](https://nuget.org/packages/)


Vermenigvuldigt de coëfficiënt van alle termen in een `GeneratorSystem` .

```qsharp
function MultiplyGeneratorSystem (multiplier : Double, generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Invoer

### <a name="multiplier--double"></a>vermenigvuldiger: [dubbel](xref:microsoft.quantum.lang-ref.double)

De vermenigvuldiger op de coëfficiënt.


### <a name="generatorsystem--generatorsystem"></a>generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

De `GeneratorSystem` te vermenigvuldigen.



## <a name="output--generatorsystem"></a>Uitvoer: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Een `GeneratorSystem` van een systeem met een coëfficiënt die groter is dan een `multiplier` grotere factor.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. simulatie. GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)