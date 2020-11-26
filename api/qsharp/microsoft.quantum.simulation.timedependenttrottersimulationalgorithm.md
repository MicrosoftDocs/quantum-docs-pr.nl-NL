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
# <a name="timedependenttrottersimulationalgorithm-function"></a>De functie TimeDependentTrotterSimulationAlgorithm

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


`TimeDependentSimulationAlgorithm` functie die gebruikmaakt van een Trotter-Suzuki-ontleding om een unitary-operator te benaderen waarmee de tijdgebonden Schrodinger vergelijking wordt opgelost.

```qsharp
function TimeDependentTrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm
```


## <a name="input"></a>Invoer

### <a name="trotterstepsize--double"></a>trotterStepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)

Duur van gesimuleerde tijd-ontwikkeling in één Trotter stap.


### <a name="trotterorder--int"></a>trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)

Volg orde van Trotter integrator. Dit moet 1 of een even getal zijn.



## <a name="output--timedependentsimulationalgorithm"></a>Uitvoer: [TimeDependentSimulationAlgorithm](xref:Microsoft.Quantum.Simulation.TimeDependentSimulationAlgorithm)

Een `TimeDependentSimulationAlgorithm` type.