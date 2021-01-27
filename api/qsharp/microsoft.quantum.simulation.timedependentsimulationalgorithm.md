---
uid: Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
title: Door de gebruiker gedefinieerd TimeDependentSimulationAlgorithm-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentSimulationAlgorithm
qsharp.summary: >-
  Represents a time-dependent simulation algorithm.

  A time-dependent simulation technique converts an <xref:microsoft.quantum.simulation.evolutionschedule> to unitary time-evolution for some time-interval.
ms.openlocfilehash: 4f393c958e686f2ded3bf3372ff9fd52b2a363cd
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854123"
---
# <a name="timedependentsimulationalgorithm-user-defined-type"></a><span data-ttu-id="33caa-102">Door de gebruiker gedefinieerd TimeDependentSimulationAlgorithm-type</span><span class="sxs-lookup"><span data-stu-id="33caa-102">TimeDependentSimulationAlgorithm user defined type</span></span>

<span data-ttu-id="33caa-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="33caa-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="33caa-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="33caa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="33caa-105">Vertegenwoordigt een tijd afhankelijke simulatie algoritme.</span><span class="sxs-lookup"><span data-stu-id="33caa-105">Represents a time-dependent simulation algorithm.</span></span>

<span data-ttu-id="33caa-106">Een tijdgebonden simulatie techniek converteert een <xref:microsoft.quantum.simulation.evolutionschedule></span><span class="sxs-lookup"><span data-stu-id="33caa-106">A time-dependent simulation technique converts an <xref:microsoft.quantum.simulation.evolutionschedule></span></span>
<span data-ttu-id="33caa-107">unitary tijd-ontwikkeling voor enige tijd interval.</span><span class="sxs-lookup"><span data-stu-id="33caa-107">to unitary time-evolution for some time-interval.</span></span>

```qsharp

newtype TimeDependentSimulationAlgorithm = (((Double, Microsoft.Quantum.Simulation.EvolutionSchedule, Qubit[]) => Unit is Adj + Ctl));
```

