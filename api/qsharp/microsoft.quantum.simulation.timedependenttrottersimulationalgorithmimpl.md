---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithmImpl
title: Bewerking TimeDependentTrotterSimulationAlgorithmImpl
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithmImpl
qsharp.summary: Implementation of multiple Trotter steps to approximate a unitary operator that solves the time-dependent Schrödinger equation.
ms.openlocfilehash: c6d1c976d29c69d3ac14d9a2be09826602c8cc1d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706436"
---
# <a name="timedependenttrottersimulationalgorithmimpl-operation"></a><span data-ttu-id="165ed-102">Bewerking TimeDependentTrotterSimulationAlgorithmImpl</span><span class="sxs-lookup"><span data-stu-id="165ed-102">TimeDependentTrotterSimulationAlgorithmImpl operation</span></span>

<span data-ttu-id="165ed-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="165ed-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="165ed-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="165ed-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="165ed-105">Implementatie van meerdere Trotter-stappen om een unitary-operator te benaderen waarmee de tijdgebonden Schrödinger-vergelijking wordt opgelost.</span><span class="sxs-lookup"><span data-stu-id="165ed-105">Implementation of multiple Trotter steps to approximate a unitary operator that solves the time-dependent Schrödinger equation.</span></span>

```qsharp
operation TimeDependentTrotterSimulationAlgorithmImpl (trotterStepSize : Double, trotterOrder : Int, maxTime : Double, evolutionSchedule : Microsoft.Quantum.Simulation.EvolutionSchedule, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="165ed-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="165ed-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="165ed-107">trotterStepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="165ed-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="165ed-108">Duur van gesimuleerde tijd-ontwikkeling in één Trotter stap.</span><span class="sxs-lookup"><span data-stu-id="165ed-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="165ed-109">trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="165ed-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="165ed-110">Volg orde van Trotter integrator.</span><span class="sxs-lookup"><span data-stu-id="165ed-110">Order of Trotter integrator.</span></span> <span data-ttu-id="165ed-111">Dit moet 1 of een even getal zijn.</span><span class="sxs-lookup"><span data-stu-id="165ed-111">This must be either 1 or an even number.</span></span>


### <a name="maxtime--double"></a><span data-ttu-id="165ed-112">maxTime: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="165ed-112">maxTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="165ed-113">Totale duur van simulatie $t $.</span><span class="sxs-lookup"><span data-stu-id="165ed-113">Total duration of simulation $t$.</span></span>


### <a name="evolutionschedule--evolutionschedule"></a><span data-ttu-id="165ed-114">evolutionSchedule: [evolutionSchedule](xref:Microsoft.Quantum.Simulation.EvolutionSchedule)</span><span class="sxs-lookup"><span data-stu-id="165ed-114">evolutionSchedule : [EvolutionSchedule](xref:Microsoft.Quantum.Simulation.EvolutionSchedule)</span></span>

<span data-ttu-id="165ed-115">Een volledige beschrijving van het tijdgebonden systeem dat moet worden gesimuleerd.</span><span class="sxs-lookup"><span data-stu-id="165ed-115">A complete description of the time-dependent system to be simulated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="165ed-116">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="165ed-116">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="165ed-117">Qubits heeft gehandeld op basis van simulatie.</span><span class="sxs-lookup"><span data-stu-id="165ed-117">Qubits acted on by simulation.</span></span>



## <a name="output--unit"></a><span data-ttu-id="165ed-118">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="165ed-118">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

