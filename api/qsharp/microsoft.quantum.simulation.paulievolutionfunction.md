---
uid: Microsoft.Quantum.Simulation.PauliEvolutionFunction
title: De functie PauliEvolutionFunction
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.
ms.openlocfilehash: 060f4e4f23bb8b47518a3a22bbca8ab0be6e13b7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706661"
---
# <a name="paulievolutionfunction-function"></a><span data-ttu-id="86a54-102">De functie PauliEvolutionFunction</span><span class="sxs-lookup"><span data-stu-id="86a54-102">PauliEvolutionFunction function</span></span>

<span data-ttu-id="86a54-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="86a54-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="86a54-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="86a54-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="86a54-105">Dit object vertegenwoordigt een dynamische generator als een set simulatieve Gates en een uitbrei ding in de Pauli basis.</span><span class="sxs-lookup"><span data-stu-id="86a54-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.</span></span>

```qsharp
function PauliEvolutionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="86a54-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="86a54-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="86a54-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="86a54-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="86a54-108">Een generator index die wordt weer gegeven als unitary-ontwikkeling in de Pauli-basis.</span><span class="sxs-lookup"><span data-stu-id="86a54-108">A generator index to be represented as unitary evolution in the Pauli basis.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="86a54-109">Uitvoer: [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="86a54-109">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="86a54-110">Een `EvolutionUnitary` representatieve tijd ontwikkeling op basis van de term waarnaar wordt verwezen in generatorIndex.</span><span class="sxs-lookup"><span data-stu-id="86a54-110">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>