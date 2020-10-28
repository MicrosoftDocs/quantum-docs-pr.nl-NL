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
# <a name="trottersimulationalgorithm-function"></a>De functie TrotterSimulationAlgorithm

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket [](https://nuget.org/packages/)


`SimulationAlgorithm` functie waarbij gebruik wordt gemaakt van een Trotter-Suzuki-ontleding om de time-evolutie operator _exp (-iHt)_ te benaderen.

```qsharp
function TrotterSimulationAlgorithm (trotterStepSize : Double, trotterOrder : Int) : Microsoft.Quantum.Simulation.SimulationAlgorithm
```


## <a name="input"></a>Invoer

### <a name="trotterstepsize--double"></a>trotterStepSize: [dubbel](xref:microsoft.quantum.lang-ref.double)

Duur van gesimuleerde tijd-ontwikkeling in één Trotter stap.


### <a name="trotterorder--int"></a>trotterOrder: [int](xref:microsoft.quantum.lang-ref.int)

Volg orde van Trotter integrator. Dit moet 1 of een even getal zijn.



## <a name="output--simulationalgorithm"></a>Uitvoer: [SimulationAlgorithm](xref:Microsoft.Quantum.Simulation.SimulationAlgorithm)

Een `SimulationAlgorithm` type.