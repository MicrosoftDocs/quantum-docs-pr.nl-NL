---
uid: Microsoft.Quantum.Simulation.PauliEvolutionSet
title: De functie PauliEvolutionSet
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 89c81aca4cfad6087d764ac8f5a0f1426e905e4b
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707813"
---
# <a name="paulievolutionset-function"></a>De functie PauliEvolutionSet

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket [](https://nuget.org/packages/)


Dit object vertegenwoordigt een dynamische generator als een set simulatieve Gates en een uitbrei ding in de Pauli basis.

```qsharp
function PauliEvolutionSet () : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="output--evolutionset"></a>Uitvoer: [evolutieset](xref:Microsoft.Quantum.Simulation.EvolutionSet)

Een `EvolutionSet` waarmee een `GeneratorIndex` voor de Pauli wordt toegewezen aan een EvolutionUnitary.

## <a name="remarks"></a>Opmerkingen

Dit wordt verkregen door gedeeltelijke toepassing van <xref:microsoft.quantum.simulation.paulievolutionfunction> .