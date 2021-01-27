---
uid: Microsoft.Quantum.Simulation.SumGeneratorSystems
title: De functie SumGeneratorSystems
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SumGeneratorSystems
qsharp.summary: Adds multiple `GeneratorSystem`s to create a new GeneratorSystem.
ms.openlocfilehash: 0e64d2b599c55c19711208670030fd01e09aff7e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851024"
---
# <a name="sumgeneratorsystems-function"></a>De functie SumGeneratorSystems

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


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