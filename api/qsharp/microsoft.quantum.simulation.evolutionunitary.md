---
uid: Microsoft.Quantum.Simulation.EvolutionUnitary
title: Door de gebruiker gedefinieerd EvolutionUnitary-type
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionUnitary
qsharp.summary: >-
  Represents a unitary time-evolution operator.

  The first parameter is is duration of time-evolution, and the second parameter is the qubit register acted upon by the unitary.
ms.openlocfilehash: 28ab492573b67e4aa42392e4ee499596b9c0225f
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709018"
---
# <a name="evolutionunitary-user-defined-type"></a>Door de gebruiker gedefinieerd EvolutionUnitary-type

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket [](https://nuget.org/packages/)


Vertegenwoordigt een unitary tijd-ontwikkelings operator.

De eerste para meter is duur van tijd-ontwikkeling en de tweede para meter is het Qubit-REGI ster dat door de unitary wordt verwerkt.

```qsharp

newtype EvolutionUnitary = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

