---
uid: Microsoft.Quantum.Simulation.GeneratorIndex
title: Door de gebruiker gedefinieerd GeneratorIndex-type
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorIndex
qsharp.summary: >-
  Represents a single primitive term in the set of all dynamical generators, e.g. Hermitian operators, for which there exists a map from that generator to time-evolution by that generator, through `EvolutionSet`.

  The first element (Int[], Double[]) is indexes that single term -- For instance, the Pauli string XXY with coefficient 0.5 would be indexed by ([1,1,2], [0.5]). Alternatively, Hamiltonians parameterized by a continuous variable, such as X cos φ + Y sin φ, might for instance be represented by ([], [φ]). The second element indexes the subsystem on which the generator acts on.
ms.openlocfilehash: dae23db9bee34be4aa99d96799efad64a66d7193
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229321"
---
# <a name="generatorindex-user-defined-type"></a>Door de gebruiker gedefinieerd GeneratorIndex-type

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dit object vertegenwoordigt een enkele primitieve term in de set met alle dynamische generatoren, zoals Hermitian-Opera Tors, waarvoor er een kaart van die generator bestaat en dat deze door de generator kan worden gepasseerd, tot en met `EvolutionSet` .

Het eerste element (int [], double []) is indices met één term. de Pauli teken reeks XXY met coëfficiënt 0,5 zou worden geïndexeerd door ([1, 1, 2], [0,5]). Het is ook mogelijk dat Hamiltonians para meters door een continue variabele, zoals X cos φ + Y Sin φ, worden vertegenwoordigd door ([], [φ]). Het tweede element indexeert het subsysteem waarop de generator werkt.

```qsharp

newtype GeneratorIndex = ((Int[], Double[]), Int[]);
```



## <a name="remarks"></a>Opmerkingen

> [!WARNING]
> De interpretatie van een `GeneratorIndex` wordt niet gedefinieerd, behalve met verwijzing naar een bepaalde set met Generators.

## <a name="see-also"></a>Zie ook

- [Micro soft. Quantum. simulatie.-ontwikkelings](xref:Microsoft.Quantum.Simulation.EvolutionSet)
- [Micro soft. Quantum. simulatie. PauliEvolutionSet](xref:Microsoft.Quantum.Simulation.PauliEvolutionSet)