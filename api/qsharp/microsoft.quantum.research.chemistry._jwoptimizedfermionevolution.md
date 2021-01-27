---
uid: Microsoft.Quantum.Research.Chemistry._JWOptimizedFermionEvolution
title: _JWOptimizedFermionEvolution bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Research.Chemistry
qsharp.name: _JWOptimizedFermionEvolution
qsharp.summary: >-
  Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.

  See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.
ms.openlocfilehash: 62fbd27f703a17a547d94e61c7a4981230a4b251
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854823"
---
# <a name="_jwoptimizedfermionevolution-operation"></a><span data-ttu-id="3686d-102">_JWOptimizedFermionEvolution bewerking</span><span class="sxs-lookup"><span data-stu-id="3686d-102">_JWOptimizedFermionEvolution operation</span></span>

<span data-ttu-id="3686d-103">Naam ruimte: [micro soft. Quantum. Research. chemie](xref:Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="3686d-103">Namespace: [Microsoft.Quantum.Research.Chemistry](xref:Microsoft.Quantum.Research.Chemistry)</span></span>

<span data-ttu-id="3686d-104">Pakket: [micro soft. Quantum. Research. chemie](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="3686d-104">Package: [Microsoft.Quantum.Research.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Research.Chemistry)</span></span>


<span data-ttu-id="3686d-105">Dit object vertegenwoordigt een dynamische generator als een set simulatieve Gates en een uitbrei ding in de JWOptimized basis.</span><span class="sxs-lookup"><span data-stu-id="3686d-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JWOptimized basis.</span></span>

<span data-ttu-id="3686d-106">Zie [model lering van dynamische Generator](../libraries/data-structures#dynamical-generator-modeling) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="3686d-106">See [Dynamical Generator Modeling](../libraries/data-structures#dynamical-generator-modeling) for more details.</span></span>

```qsharp
operation _JWOptimizedFermionEvolution (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex, stepSize : Double, parityQubit : Qubit, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="3686d-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="3686d-107">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="3686d-108">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="3686d-108">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="3686d-109">Een generator index die wordt weer gegeven als unitary-ontwikkeling in de JWOptimized-basis.</span><span class="sxs-lookup"><span data-stu-id="3686d-109">A generator index to be represented as unitary evolution in the JWOptimized basis.</span></span>


### <a name="stepsize--double"></a><span data-ttu-id="3686d-110">stepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="3686d-110">stepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="3686d-111">Een vermenigvuldigings factor voor de duur van de tijd in de periode waarnaar wordt verwezen in `generatorIndex` .</span><span class="sxs-lookup"><span data-stu-id="3686d-111">A multiplier on the duration of time-evolution by the term referenced in `generatorIndex`.</span></span>


### <a name="parityqubit--qubit"></a><span data-ttu-id="3686d-112">parityQubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="3686d-112">parityQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="3686d-113">Qubit die het teken van de tijd ontwikkeling bepaalt.</span><span class="sxs-lookup"><span data-stu-id="3686d-113">Qubit that determines the sign of time-evolution.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="3686d-114">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="3686d-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="3686d-115">Registratie van de actie op basis van tijd-ontwikkelings operator.</span><span class="sxs-lookup"><span data-stu-id="3686d-115">Register acted upon by time-evolution operator.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3686d-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3686d-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

