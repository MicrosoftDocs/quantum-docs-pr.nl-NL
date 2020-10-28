---
uid: Microsoft.Quantum.Simulation.TrotterSimulationAlgorithm
title: De functie TrotterSimulationAlgorithm
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TrotterSimulationAlgorithm
qsharp.summary: '`SimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate the time-evolution operator _exp(-iHt)_.'
ms.openlocfilehash: c52acf293e69c78e7a82b0cf5d94de52d0f5a293
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706437"
---
# <a name="trottersimulationalgorithm-function"></a><span data-ttu-id="9614e-102">De functie TrotterSimulationAlgorithm</span><span class="sxs-lookup"><span data-stu-id="9614e-102">TrotterSimulationAlgorithm function</span></span>

<span data-ttu-id="9614e-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="9614e-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="9614e-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9614e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9614e-105">`SimulationAlgorithm` functie waarbij gebruik wordt gemaakt van een Trotter-Suzuki-ontleding om de time-evolutie operator _exp (-iHt)_ te benaderen.</span><span class="sxs-lookup"><span data-stu-id="9614e-105">`SimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate the time-evolution operator _exp(-iHt)_ .</span></span>

```qsharp
function TrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.SimulationAlgorithm
```


## <a name="input"></a><span data-ttu-id="9614e-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9614e-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="9614e-107">trotterStepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="9614e-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="9614e-108">Duur van gesimuleerde tijd-ontwikkeling in één Trotter stap.</span><span class="sxs-lookup"><span data-stu-id="9614e-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="9614e-109">trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9614e-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9614e-110">Volg orde van Trotter integrator.</span><span class="sxs-lookup"><span data-stu-id="9614e-110">Order of Trotter integrator.</span></span> <span data-ttu-id="9614e-111">Dit moet 1 of een even getal zijn.</span><span class="sxs-lookup"><span data-stu-id="9614e-111">This must be either 1 or an even number.</span></span>



## <a name="output--simulationalgorithm"></a><span data-ttu-id="9614e-112">Uitvoer: [SimulationAlgorithm](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="9614e-112">Output : [SimulationAlgorithm](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)</span></span>

<span data-ttu-id="9614e-113">Een `SimulationAlgorithm` type.</span><span class="sxs-lookup"><span data-stu-id="9614e-113">A `SimulationAlgorithm` type.</span></span>