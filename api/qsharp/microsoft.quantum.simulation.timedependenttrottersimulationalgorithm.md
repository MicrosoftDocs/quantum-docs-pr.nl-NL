---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithm
title: De functie TimeDependentTrotterSimulationAlgorithm
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithm
qsharp.summary: '`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.'
ms.openlocfilehash: 6129d768276b5c9d96a1b1ed9cd5a6a22d28e286
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706444"
---
# <a name="timedependenttrottersimulationalgorithm-function"></a><span data-ttu-id="694ac-102">De functie TimeDependentTrotterSimulationAlgorithm</span><span class="sxs-lookup"><span data-stu-id="694ac-102">TimeDependentTrotterSimulationAlgorithm function</span></span>

<span data-ttu-id="694ac-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="694ac-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="694ac-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="694ac-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="694ac-105">`TimeDependentSimulationAlgorithm` functie die gebruikmaakt van een Trotter-Suzuki-ontleding om een unitary-operator te benaderen waarmee de tijdgebonden Schrodinger vergelijking wordt opgelost.</span><span class="sxs-lookup"><span data-stu-id="694ac-105">`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.</span></span>

```qsharp
function TimeDependentTrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
```


## <a name="input"></a><span data-ttu-id="694ac-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="694ac-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="694ac-107">trotterStepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="694ac-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="694ac-108">Duur van gesimuleerde tijd-ontwikkeling in één Trotter stap.</span><span class="sxs-lookup"><span data-stu-id="694ac-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="694ac-109">trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="694ac-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="694ac-110">Volg orde van Trotter integrator.</span><span class="sxs-lookup"><span data-stu-id="694ac-110">Order of Trotter integrator.</span></span> <span data-ttu-id="694ac-111">Dit moet 1 of een even getal zijn.</span><span class="sxs-lookup"><span data-stu-id="694ac-111">This must be either 1 or an even number.</span></span>



## <a name="output--timedependentsimulationalgorithm"></a><span data-ttu-id="694ac-112">Uitvoer: [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="694ac-112">Output : [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span></span>

<span data-ttu-id="694ac-113">Een `TimeDependentSimulationAlgorithm` type.</span><span class="sxs-lookup"><span data-stu-id="694ac-113">A `TimeDependentSimulationAlgorithm` type.</span></span>