---
uid: Microsoft.Quantum.Simulation.GetGeneratorSystemFunction
title: De functie GetGeneratorSystemFunction
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GetGeneratorSystemFunction
qsharp.summary: Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.
ms.openlocfilehash: 60ebbdbd1020d41a54426377043fc0c84ceec504
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708887"
---
# <a name="getgeneratorsystemfunction-function"></a>De functie GetGeneratorSystemFunction

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket [](https://nuget.org/packages/)


Haalt de `GeneratorIndex` functie op in een `GeneratorSystem` .

```qsharp
function GetGeneratorSystemFunction (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)
```


## <a name="input"></a>Invoer

### <a name="generatorsystem--generatorsystem"></a>generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Het is `GeneratorSystem` van belang.



## <a name="output--int---generatorindex"></a>Uitvoer: [int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)

Een functie waarmee elke `GeneratorIndex` term in een Hamiltonian wordt geïndexeerd.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. simulatie. GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)
- [Micro soft. Quantum. simulatie. GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)