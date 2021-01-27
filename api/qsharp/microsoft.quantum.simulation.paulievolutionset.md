---
uid: Microsoft.Quantum.Simulation.PauliEvolutionSet
title: De functie PauliEvolutionSet
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionSet
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 961c95e6787b69e35ca531fa36164cc988ad660d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847966"
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