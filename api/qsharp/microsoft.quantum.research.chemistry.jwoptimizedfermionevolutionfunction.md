---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedFermionEvolutionFunction
title: De functie JWOptimizedFermionEvolutionFunction
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedFermionEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.
ms.openlocfilehash: 952f3dc4ab0595ace0ee34c040cb21969afa111f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701823"
---
# <a name="jwoptimizedfermionevolutionfunction-function"></a><span data-ttu-id="12ebf-102">De functie JWOptimizedFermionEvolutionFunction</span><span class="sxs-lookup"><span data-stu-id="12ebf-102">JWOptimizedFermionEvolutionFunction function</span></span>

<span data-ttu-id="12ebf-103">Naam ruimte: [micro soft. Quantum. Research. chemie](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="12ebf-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="12ebf-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="12ebf-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="12ebf-105">Dit object vertegenwoordigt een dynamische generator als een set simulatieve Gates en een uitbrei ding in de JWOptimized basis.</span><span class="sxs-lookup"><span data-stu-id="12ebf-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.</span></span>

```qsharp
function JWOptimizedFermionEvolutionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="12ebf-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="12ebf-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="12ebf-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="12ebf-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="12ebf-108">Een generator index die wordt weer gegeven als unitary-ontwikkeling in de JWOptimized-basis.</span><span class="sxs-lookup"><span data-stu-id="12ebf-108">A generator index to be represented as unitary evolution in the JWOptimized basis.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="12ebf-109">parityQubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="12ebf-109">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="12ebf-110">Qubit die het teken van de tijd ontwikkeling bepaalt.</span><span class="sxs-lookup"><span data-stu-id="12ebf-110">Qubit that determines the sign of time-evolution.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="12ebf-111">Uitvoer: [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="12ebf-111">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="12ebf-112">Een `EvolutionUnitary` representatieve tijd ontwikkeling op basis van de term waarnaar wordt verwezen in generatorIndex.</span><span class="sxs-lookup"><span data-stu-id="12ebf-112">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>