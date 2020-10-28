---
uid: Microsoft.Quantum.Simulation.InterpolatedEvolution
title: De functie InterpolatedEvolution
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolatedEvolution
qsharp.summary: Interpolates between two generators with a uniform schedule, returning an operation that applies simulated evolution under the resulting time-dependent generator to a qubit register.
ms.openlocfilehash: 18026b9872f6a3344a1e5c2122f55927975ccb59
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701732"
---
# <a name="interpolatedevolution-function"></a><span data-ttu-id="46674-102">De functie InterpolatedEvolution</span><span class="sxs-lookup"><span data-stu-id="46674-102">InterpolatedEvolution function</span></span>

<span data-ttu-id="46674-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="46674-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="46674-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="46674-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="46674-105">Interpoleert twee generatoren met een uniform schema, waarbij een bewerking wordt geretourneerd waarmee gesimuleerde evoluties worden toegepast onder de resulterende tijd afhankelijke Generator naar een Qubit-REGI ster.</span><span class="sxs-lookup"><span data-stu-id="46674-105">Interpolates between two generators with a uniform schedule, returning an operation that applies simulated evolution under the resulting time-dependent generator to a qubit register.</span></span>

```qsharp
function InterpolatedEvolution (interpolationTime : Double, evolutionGeneratorStart : Microsoft.Quantum.Simulation.EvolutionGenerator, evolutionGeneratorEnd : Microsoft.Quantum.Simulation.EvolutionGenerator, timeDependentSimulationAlgorithm : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="46674-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="46674-106">Input</span></span>

### <a name="interpolationtime--double"></a><span data-ttu-id="46674-107">interpolationTime: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="46674-107">interpolationTime : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="46674-108">Tijd waarop de interpolatie moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="46674-108">Time to perform the interpolation over.</span></span>


### <a name="evolutiongeneratorstart--evolutiongenerator"></a><span data-ttu-id="46674-109">evolutionGeneratorStart: [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="46674-109">evolutionGeneratorStart : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="46674-110">Initiële generator voor het simuleren van de ontwikkeling onder.</span><span class="sxs-lookup"><span data-stu-id="46674-110">Initial generator to simulate evolution under.</span></span>


### <a name="evolutiongeneratorend--evolutiongenerator"></a><span data-ttu-id="46674-111">evolutionGeneratorEnd: [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="46674-111">evolutionGeneratorEnd : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="46674-112">Definitieve generator voor het simuleren van de ontwikkeling onder.</span><span class="sxs-lookup"><span data-stu-id="46674-112">Final generator to simulate evolution under.</span></span>


### <a name="timedependentsimulationalgorithm--timedependentsimulationalgorithm"></a><span data-ttu-id="46674-113">timeDependentSimulationAlgorithm: [timeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="46674-113">timeDependentSimulationAlgorithm : [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span></span>

<span data-ttu-id="46674-114">Een tijdgebonden simulatie algoritme dat wordt gebruikt voor het simuleren van de evolutie tijdens het uniforme interpolatie schema.</span><span class="sxs-lookup"><span data-stu-id="46674-114">A time-dependent simulation algorithm that will be used to simulate evolution during the uniform interpolation schedule.</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="46674-115">Output: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="46674-115">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>



## <a name="remarks"></a><span data-ttu-id="46674-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="46674-116">Remarks</span></span>

<span data-ttu-id="46674-117">Als de interpolatie tijd is gekozen om te voldoen aan de Adiabatic-voor waarden, retourneert deze functie een bewerking die Adiabatic-status voorbereiding uitvoert voor de laatste dynamische generator.</span><span class="sxs-lookup"><span data-stu-id="46674-117">If the interpolation time is chosen to meet the adiabatic conditions, then this function returns an operation which performs adiabatic state preparation for the final dynamical generator.</span></span>