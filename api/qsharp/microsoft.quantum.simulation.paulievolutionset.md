---
uid: Microsoft.Quantum.Simulation.PauliEvolutionSet
title: De functie PauliEvolutionSet
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: fb53b90b6ab5ce1003f66b68a8c2ad8b3631f627
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230342"
---
# <a name="paulievolutionset-function"></a>De functie PauliEvolutionSet

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Dit object vertegenwoordigt een dynamische generator als een set simulatieve Gates en een uitbrei ding in de Pauli basis.

```qsharp
function PauliEvolutionSet () : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="output--evolutionset"></a>Uitvoer: [evolutieset](xref:Microsoft.Quantum.Simulation.EvolutionSet)

Een `EvolutionSet` waarmee een `GeneratorIndex` voor de Pauli wordt toegewezen aan een EvolutionUnitary.

## <a name="remarks"></a>Opmerkingen

Dit wordt verkregen door gedeeltelijke toepassing van <xref:microsoft.quantum.simulation.paulievolutionfunction> .