---
uid: Microsoft.Quantum.Simulation.TrotterStep
title: De functie TrotterStep
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterStep
qsharp.summary: Implements a single time-step of time-evolution by the system described in an `EvolutionGenerator` using a Trotter–Suzuki decomposition.
ms.openlocfilehash: 7a1a27ba4dc4b8b7bbc4da6a378d4a1494bc9415
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709229"
---
# <a name="trotterstep-function"></a><span data-ttu-id="2507d-102">De functie TrotterStep</span><span class="sxs-lookup"><span data-stu-id="2507d-102">TrotterStep function</span></span>

<span data-ttu-id="2507d-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="2507d-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="2507d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="2507d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="2507d-105">Implementeert een eenmalige stap van tijd-ontwikkeling door het systeem dat wordt beschreven in een `EvolutionGenerator` Trotter – Suzuki-ontleding.</span><span class="sxs-lookup"><span data-stu-id="2507d-105">Implements a single time-step of time-evolution by the system described in an `EvolutionGenerator` using a Trotter–Suzuki decomposition.</span></span>

```qsharp
function TrotterStep (evolutionGenerator : Microsoft.Quantum.Simulation.EvolutionGenerator, trotterOrder : Int, trotterStepSize : Double) : (Qubit[] => Unit is Adj + Ctl)
```


## <a name="input"></a><span data-ttu-id="2507d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="2507d-106">Input</span></span>

### <a name="evolutiongenerator--evolutiongenerator"></a><span data-ttu-id="2507d-107">evolutionGenerator: [evolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span><span class="sxs-lookup"><span data-stu-id="2507d-107">evolutionGenerator : [EvolutionGenerator](xref:Microsoft.Quantum.Simulation.EvolutionGenerator)</span></span>

<span data-ttu-id="2507d-108">Een volledige beschrijving van het systeem dat moet worden gesimuleerd.</span><span class="sxs-lookup"><span data-stu-id="2507d-108">A complete description of the system to be simulated.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="2507d-109">trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2507d-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2507d-110">Volg orde van Trotter integrator.</span><span class="sxs-lookup"><span data-stu-id="2507d-110">Order of Trotter integrator.</span></span> <span data-ttu-id="2507d-111">Dit moet 1 of een even getal zijn.</span><span class="sxs-lookup"><span data-stu-id="2507d-111">This must be either 1 or an even number.</span></span>


### <a name="trotterstepsize--double"></a><span data-ttu-id="2507d-112">trotterStepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="2507d-112">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="2507d-113">Duur van gesimuleerde tijd-ontwikkeling in één Trotter stap.</span><span class="sxs-lookup"><span data-stu-id="2507d-113">Duration of simulated time-evolution in single Trotter step.</span></span>



## <a name="output--qubit--unit-adj--ctl"></a><span data-ttu-id="2507d-114">Output: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="2507d-114">Output : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="2507d-115">Een unitary-bewerking die een enkele stap van tijd-ontwikkeling voor de duur van de periode benadert `trotterStepSize` .</span><span class="sxs-lookup"><span data-stu-id="2507d-115">Unitary operation that approximates a single step of time-evolution for duration `trotterStepSize`.</span></span>

## <a name="remarks"></a><span data-ttu-id="2507d-116">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="2507d-116">Remarks</span></span>

<span data-ttu-id="2507d-117">Zie voor meer informatie over de ontleding van de Trotter-Suzuki een [geordende samen stelling](/quantum/libraries/control-flow#time-ordered-composition).</span><span class="sxs-lookup"><span data-stu-id="2507d-117">For more on the Trotter–Suzuki decomposition, see [Time-Ordered Composition](/quantum/libraries/control-flow#time-ordered-composition).</span></span>