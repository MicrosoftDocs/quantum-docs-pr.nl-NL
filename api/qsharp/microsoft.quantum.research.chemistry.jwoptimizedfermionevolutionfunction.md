---
uid: Microsoft.Quantum.Research.Chemistry.JWOptimizedFermionEvolutionFunction
title: De functie JWOptimizedFermionEvolutionFunction
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: JWOptimizedFermionEvolutionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.
ms.openlocfilehash: d70bea8fcb5bd82ddad6dcd2b67c3eb178283bb3
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98857863"
---
# <a name="jwoptimizedfermionevolutionfunction-function"></a><span data-ttu-id="59ff5-102">De functie JWOptimizedFermionEvolutionFunction</span><span class="sxs-lookup"><span data-stu-id="59ff5-102">JWOptimizedFermionEvolutionFunction function</span></span>

<span data-ttu-id="59ff5-103">Naam ruimte: [micro soft. Quantum. Research. chemie](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="59ff5-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="59ff5-104">Pakket: [micro soft. Quantum. Research. chemie](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="59ff5-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="59ff5-105">Dit object vertegenwoordigt een dynamische generator als een set simulatieve Gates en een uitbrei ding in de JWOptimized basis.</span><span class="sxs-lookup"><span data-stu-id="59ff5-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.</span></span>

```qsharp
function JWOptimizedFermionEvolutionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, parityQubit : Qubit) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="59ff5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="59ff5-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="59ff5-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="59ff5-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="59ff5-108">Een generator index die wordt weer gegeven als unitary-ontwikkeling in de JWOptimized-basis.</span><span class="sxs-lookup"><span data-stu-id="59ff5-108">A generator index to be represented as unitary evolution in the JWOptimized basis.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="59ff5-109">parityQubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="59ff5-109">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="59ff5-110">Qubit die het teken van de tijd ontwikkeling bepaalt.</span><span class="sxs-lookup"><span data-stu-id="59ff5-110">Qubit that determines the sign of time-evolution.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="59ff5-111">Uitvoer: [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="59ff5-111">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="59ff5-112">Een `EvolutionUnitary` representatieve tijd ontwikkeling op basis van de term waarnaar wordt verwezen in generatorIndex.</span><span class="sxs-lookup"><span data-stu-id="59ff5-112">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>