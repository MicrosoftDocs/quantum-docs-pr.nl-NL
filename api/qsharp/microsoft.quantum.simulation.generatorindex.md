---
uid: Microsoft.Quantum.Simulation.GeneratorIndex
title: Door de gebruiker gedefinieerd GeneratorIndex-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GeneratorIndex
qsharp.summary: >-
  Represents a single primitive term in the set of all dynamical generators, e.g. Hermitian operators, for which there exists a map from that generator to time-evolution by that generator, through `EvolutionSet`.

  The first element (Int[], Double[]) is indexes that single term -- For instance, the Pauli string XXY with coefficient 0.5 would be indexed by ([1,1,2], [0.5]). Alternatively, Hamiltonians parameterized by a continuous variable, such as X cos φ + Y sin φ, might for instance be represented by ([], [φ]). The second element indexes the subsystem on which the generator acts on.
ms.openlocfilehash: 8d36f74fbf122469e9e829b950e4ed9a6e3a35a7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708610"
---
# <a name="generatorindex-user-defined-type"></a>Door de gebruiker gedefinieerd GeneratorIndex-type

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket [](https://nuget.org/packages/)


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