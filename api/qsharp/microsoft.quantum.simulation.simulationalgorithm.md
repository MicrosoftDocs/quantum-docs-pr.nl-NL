---
uid: Microsoft.Quantum.Simulation.SimulationAlgorithm
title: Door de gebruiker gedefinieerd SimulationAlgorithm-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: SimulationAlgorithm
qsharp.summary: >-
  Represents a time-independent simulation algorithm.

  A time-independent simulation technique converts an <xref:microsoft.quantum.simulation.evolutiongenerator> to unitary time evolution for some time-interval.
ms.openlocfilehash: 9127a936bbf7a212e712645eabdf49fefc7a97d0
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709324"
---
# <a name="simulationalgorithm-user-defined-type"></a>Door de gebruiker gedefinieerd SimulationAlgorithm-type

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket [](https://nuget.org/packages/)


Vertegenwoordigt een tijd onafhankelijk simulatie algoritme.

Met een tijd onafhankelijke simulatie methode wordt een <xref:microsoft.quantum.simulation.evolutiongenerator>
unitary tijd-ontwikkeling voor enige tijd interval.

```qsharp

newtype SimulationAlgorithm = (((Double, Microsoft.Quantum.Simulation.EvolutionGenerator, Qubit[]) => Unit is Adj + Ctl));
```

