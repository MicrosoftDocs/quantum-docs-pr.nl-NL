---
uid: Microsoft.Quantum.Simulation.TimeDependentTrotterSimulationAlgorithm
title: De functie TimeDependentTrotterSimulationAlgorithm
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentTrotterSimulationAlgorithm
qsharp.summary: '`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.'
ms.openlocfilehash: 94bc606fdc46d77e8beb1470c78102a63e6d4e81
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96192771"
---
# <a name="timedependenttrottersimulationalgorithm-function"></a><span data-ttu-id="e4d70-102">De functie TimeDependentTrotterSimulationAlgorithm</span><span class="sxs-lookup"><span data-stu-id="e4d70-102">TimeDependentTrotterSimulationAlgorithm function</span></span>

<span data-ttu-id="e4d70-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="e4d70-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="e4d70-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e4d70-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e4d70-105">`TimeDependentSimulationAlgorithm` functie die gebruikmaakt van een Trotter-Suzuki-ontleding om een unitary-operator te benaderen waarmee de tijdgebonden Schrodinger vergelijking wordt opgelost.</span><span class="sxs-lookup"><span data-stu-id="e4d70-105">`TimeDependentSimulationAlgorithm` function that uses a Trotter–Suzuki decomposition to approximate a unitary operator that solves the time-dependent Schrodinger equation.</span></span>

```qsharp
function TimeDependentTrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
```


## <a name="input"></a><span data-ttu-id="e4d70-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e4d70-106">Input</span></span>

### <a name="trotterstepsize--double"></a><span data-ttu-id="e4d70-107">trotterStepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e4d70-107">trotterStepSize : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e4d70-108">Duur van gesimuleerde tijd-ontwikkeling in één Trotter stap.</span><span class="sxs-lookup"><span data-stu-id="e4d70-108">Duration of simulated time-evolution in single Trotter step.</span></span>


### <a name="trotterorder--int"></a><span data-ttu-id="e4d70-109">trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e4d70-109">trotterOrder : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e4d70-110">Volg orde van Trotter integrator.</span><span class="sxs-lookup"><span data-stu-id="e4d70-110">Order of Trotter integrator.</span></span> <span data-ttu-id="e4d70-111">Dit moet 1 of een even getal zijn.</span><span class="sxs-lookup"><span data-stu-id="e4d70-111">This must be either 1 or an even number.</span></span>



## <a name="output--timedependentsimulationalgorithm"></a><span data-ttu-id="e4d70-112">Uitvoer: [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span><span class="sxs-lookup"><span data-stu-id="e4d70-112">Output : [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)</span></span>

<span data-ttu-id="e4d70-113">Een `TimeDependentSimulationAlgorithm` type.</span><span class="sxs-lookup"><span data-stu-id="e4d70-113">A `TimeDependentSimulationAlgorithm` type.</span></span>