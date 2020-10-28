---
uid: Microsoft.Quantum.Simulation.SumGeneratorSystems
title: De functie SumGeneratorSystems
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SumGeneratorSystems
qsharp.summary: Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.
ms.openlocfilehash: b667a6af313b5bb8950a34a6d0406976bde49311
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706452"
---
# <a name="sumgeneratorsystems-function"></a>De functie SumGeneratorSystems

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket [](https://nuget.org/packages/)


Voegt meerdere `GeneratorSystem` s toe om een nieuwe GeneratorSystem te maken.

```qsharp
function SumGeneratorSystems (generatorSystems : Microsoft.Quantum.Simulation.GeneratorSystem[]) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a>Invoer

### <a name="generatorsystems--generatorsystem"></a>generatorSystems: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)[]

Een matrix van het type `GeneratorSystem[]` .



## <a name="output--generatorsystem"></a>Uitvoer: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)

Een `GeneratorSystem` die een systeem vertegenwoordigt dat de som is van de invoer Generator systemen.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. simulatie. GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)