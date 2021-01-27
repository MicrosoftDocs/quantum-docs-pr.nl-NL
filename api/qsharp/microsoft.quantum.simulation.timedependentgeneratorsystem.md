---
uid: Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
title: Door de gebruiker gedefinieerd TimeDependentGeneratorSystem-type
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: TimeDependentGeneratorSystem
qsharp.summary: Represents a time-dependent dynamical generator as a function from time to the value of the dynamical generator at that time.
ms.openlocfilehash: dbbbb2b67dcf191c74e593f61eb894192acb4d48
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98854732"
---
# <a name="timedependentgeneratorsystem-user-defined-type"></a>Door de gebruiker gedefinieerd TimeDependentGeneratorSystem-type

Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)

Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)


Vertegenwoordigt een tijd afhankelijke dynamische generator als een functie van tijd tot de waarde van de dynamische generator op dat moment.

```qsharp

newtype TimeDependentGeneratorSystem = ((Double -> Microsoft.Quantum.Simulation.GeneratorSystem));
```

