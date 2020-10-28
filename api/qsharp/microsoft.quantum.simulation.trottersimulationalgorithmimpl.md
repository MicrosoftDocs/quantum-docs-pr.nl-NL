---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithmImpl
title: Bewerking TrotterSimulationAlgorithmImpl
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithmImpl
qsharp.summary: Makes repeated calls to `TrotterStep` to approximate the time-evolution operator exp(_-iHt_).
ms.openlocfilehash: 2af68532d700a1fb5b037707ce4650696cbe1a64
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709234"
---
# <a name="trottersimulationalgorithmimpl-operation"></a><span data-ttu-id="43265-102">Bewerking TrotterSimulationAlgorithmImpl</span><span class="sxs-lookup"><span data-stu-id="43265-102">TrotterSimulationAlgorithmImpl operation</span></span>

<span data-ttu-id="43265-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="43265-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="43265-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="43265-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="43265-105">Maakt herhaalde aanroepen om `TrotterStep` de tijd-ontwikkelings operator exp ( _-iHt_ ) te benaderen.</span><span class="sxs-lookup"><span data-stu-id="43265-105">Makes repeated calls to `TrotterStep` to approximate the time-evolution operator exp( _-iHt_ ).</span></span>

```qsharp
operation TrotterSimulationAlgorithmImpl (trotterStepSize : Double, trotterOrder : Int, maxTime : Double, evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="43265-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="43265-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="43265-107">trotterStepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="43265-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="43265-108">Duur van gesimuleerde tijd-ontwikkeling in één Trotter stap.</span><span class="sxs-lookup"><span data-stu-id="43265-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="43265-109">trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="43265-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="43265-110">Volg orde van Trotter integrator.</span><span class="sxs-lookup"><span data-stu-id="43265-110">Order of Trotter integrator.</span></span> <span data-ttu-id="43265-111">Dit moet 1 of een even getal zijn.</span><span class="sxs-lookup"><span data-stu-id="43265-111">This must be either 1 or an even number.</span></span>


### <a name="maxtime--double"></a><span data-ttu-id="43265-112">maxTime: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="43265-112">maxTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="43265-113">Totale duur van simulatie $t $.</span><span class="sxs-lookup"><span data-stu-id="43265-113">Total duration of simulation $t$.</span></span>


### <a name="evolutiongenerator--evolutiongenerator"></a><span data-ttu-id="43265-114">evolutionGenerator: [evolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="43265-114">evolutionGenerator : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="43265-115">Een volledige beschrijving van het systeem dat moet worden gesimuleerd.</span><span class="sxs-lookup"><span data-stu-id="43265-115">A complete description of the system to be simulated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="43265-116">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="43265-116">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="43265-117">Qubits heeft gehandeld op basis van simulatie.</span><span class="sxs-lookup"><span data-stu-id="43265-117">Qubits acted on by simulation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="43265-118">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="43265-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

