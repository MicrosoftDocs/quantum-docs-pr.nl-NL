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
# <a name="paulievolutionset-function"></a><span data-ttu-id="e8f29-102">De functie PauliEvolutionSet</span><span class="sxs-lookup"><span data-stu-id="e8f29-102">PauliEvolutionSet function</span></span>

<span data-ttu-id="e8f29-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="e8f29-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="e8f29-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e8f29-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e8f29-105">Dit object vertegenwoordigt een dynamische generator als een set simulatieve Gates en een uitbrei ding in de Pauli basis.</span><span class="sxs-lookup"><span data-stu-id="e8f29-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.</span></span>

```qsharp
function PauliEvolutionSet () : Microsoft.Quantum.Simulation.EvolutionSet
```


## <a name="output--evolutionset"></a><span data-ttu-id="e8f29-106">Uitvoer: [evolutieset](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span><span class="sxs-lookup"><span data-stu-id="e8f29-106">Output : [EvolutionSet](xref:Microsoft.Quantum.Simulation.EvolutionSet)</span></span>

<span data-ttu-id="e8f29-107">Een `EvolutionSet` waarmee een `GeneratorIndex` voor de Pauli wordt toegewezen aan een EvolutionUnitary.</span><span class="sxs-lookup"><span data-stu-id="e8f29-107">An `EvolutionSet` that maps a `GeneratorIndex` for the Pauli basis to an \`EvolutionUnitary.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8f29-108">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="e8f29-108">Remarks</span></span>

<span data-ttu-id="e8f29-109">Dit wordt verkregen door gedeeltelijke toepassing van <xref:microsoft.quantum.simulation.paulievolutionfunction> .</span><span class="sxs-lookup"><span data-stu-id="e8f29-109">This is obtained by partial application of <xref:microsoft.quantum.simulation.paulievolutionfunction>.</span></span>