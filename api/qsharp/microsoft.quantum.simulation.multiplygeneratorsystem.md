---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorSystem
title: De functie MultiplyGeneratorSystem
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorSystem
qsharp.summary: Multiplies the coefficient of all terms in a `GeneratorSystem`.
ms.openlocfilehash: cebd08c86ad8a3793ba7d0e9ce241d7a1ef046ae
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98858501"
---
# <a name="multiplygeneratorsystem-function"></a>De functie MultiplyGeneratorSystem

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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