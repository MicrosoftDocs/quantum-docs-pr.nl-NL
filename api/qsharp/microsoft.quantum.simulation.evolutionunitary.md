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
# <a name="evolutionunitary-user-defined-type"></a><span data-ttu-id="6f1a2-102">Door de gebruiker gedefinieerd EvolutionUnitary-type</span><span class="sxs-lookup"><span data-stu-id="6f1a2-102">EvolutionUnitary user defined type</span></span>

<span data-ttu-id="6f1a2-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="6f1a2-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="6f1a2-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6f1a2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6f1a2-105">Vertegenwoordigt een unitary tijd-ontwikkelings operator.</span><span class="sxs-lookup"><span data-stu-id="6f1a2-105">Represents a unitary time-evolution operator.</span></span>

<span data-ttu-id="6f1a2-106">De eerste para meter is duur van tijd-ontwikkeling en de tweede para meter is het Qubit-REGI ster dat door de unitary wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="6f1a2-106">The first parameter is is duration of time-evolution, and the second parameter is the qubit register acted upon by the unitary.</span></span>

```qsharp

newtype EvolutionUnitary = (((Double, Qubit[]) => Unit is Adj + Ctl));
```

