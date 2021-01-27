---
uid: Microsoft.Quantum.Simulation.EvolutionUnitary
title: Door de gebruiker gedefinieerd EvolutionUnitary-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionUnitary
qsharp.summary: >-
  Represents a unitary time-evolution operator.

  The first parameter is is duration of time-evolution, and the second parameter is the qubit register acted upon by the unitary.
ms.openlocfilehash: ea160bb9a0a8bb5106c3e37a6a16155bad71dd25
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856047"
---
# <a name="evolutionunitary-user-defined-type"></a>Door de gebruiker gedefinieerd EvolutionUnitary-type

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Vertegenwoordigt een unitary tijd-ontwikkelings operator.

De eerste para meter is duur van tijd-ontwikkeling en de tweede para meter is het Qubit-REGI ster dat door de unitary wordt verwerkt.

```qsharp

newtype EvolutionUnitary = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

