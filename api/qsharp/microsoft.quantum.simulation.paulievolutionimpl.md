---
uid: Microsoft.Quantum.Simulation.PauliEvolutionImpl
title: Bewerking PauliEvolutionImpl
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: PauliEvolutionImpl
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.

  See [Dynamical Generator Modeling](/quantum/libraries/data-structures#dynamical-generator-modeling) for more details.
ms.openlocfilehash: 2fc9fda2dd6eec71d8b17ba8a00d8545e517eec8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706668"
---
# <a name="paulievolutionimpl-operation"></a><span data-ttu-id="eb92e-102">Bewerking PauliEvolutionImpl</span><span class="sxs-lookup"><span data-stu-id="eb92e-102">PauliEvolutionImpl operation</span></span>

<span data-ttu-id="eb92e-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="eb92e-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="eb92e-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="eb92e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="eb92e-105">Dit object vertegenwoordigt een dynamische generator als een set simulatieve Gates en een uitbrei ding in de Pauli basis.</span><span class="sxs-lookup"><span data-stu-id="eb92e-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the Pauli basis.</span></span>

<span data-ttu-id="eb92e-106">Zie [model lering van dynamische Generator](/quantum/libraries/data-structures#dynamical-generator-modeling) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="eb92e-106">See [Dynamical Generator Modeling](/quantum/libraries/data-structures#dynamical-generator-modeling) for more details.</span></span>

```qsharp
operation PauliEvolutionImpl (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, delta : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="eb92e-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="eb92e-107">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="eb92e-108">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="eb92e-108">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="eb92e-109">Een generator index die wordt weer gegeven als unitary-ontwikkeling in de Pauli-basis.</span><span class="sxs-lookup"><span data-stu-id="eb92e-109">A generator index to be represented as unitary evolution in the Pauli basis.</span></span>


### <a name="delta--double"></a><span data-ttu-id="eb92e-110">verschil: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="eb92e-110">delta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="eb92e-111">Een vermenigvuldigings factor voor de duur van de tijd in de periode waarnaar wordt verwezen in `generatorIndex` .</span><span class="sxs-lookup"><span data-stu-id="eb92e-111">A multiplier on the duration of time-evolution by the term referenced in `generatorIndex`.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="eb92e-112">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="eb92e-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="eb92e-113">Registratie van de actie op basis van tijd-ontwikkelings operator.</span><span class="sxs-lookup"><span data-stu-id="eb92e-113">Register acted upon by time-evolution operator.</span></span>



## <a name="output--unit"></a><span data-ttu-id="eb92e-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="eb92e-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

