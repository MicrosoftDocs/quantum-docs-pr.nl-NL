---
uid: Microsoft.Quantum.Simulation.EvolutionSet
title: Door de gebruiker gedefinieerd type ontwikkelings
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionSet
qsharp.summary: >-
  Represents a set of gates that can be readily implemented and used to implement simulation algorithms.

  Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time
ms.openlocfilehash: 41504837b281b1021a2d09ef75acc10315b4fd07
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701744"
---
# <a name="evolutionset-user-defined-type"></a><span data-ttu-id="56190-102">Door de gebruiker gedefinieerd type ontwikkelings</span><span class="sxs-lookup"><span data-stu-id="56190-102">EvolutionSet user defined type</span></span>

<span data-ttu-id="56190-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="56190-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="56190-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="56190-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="56190-105">Vertegenwoordigt een set poorten die eenvoudig kunnen worden geïmplementeerd en gebruikt voor het implementeren van simulatie algoritmen.</span><span class="sxs-lookup"><span data-stu-id="56190-105">Represents a set of gates that can be readily implemented and used to implement simulation algorithms.</span></span>

<span data-ttu-id="56190-106">Elementen in de set worden geïndexeerd door een  <xref:microsoft.quantum.simulation.generatorindex> , en elke set wordt beschreven door een functie van `GeneratorIndex` naar  <xref:microsoft.quantum.simulation.evolutionunitary> , die para meters voor bewerkingen zijn met een reëel getal dat tijd vertegenwoordigt</span><span class="sxs-lookup"><span data-stu-id="56190-106">Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time</span></span>

```qsharp

newtype EvolutionSet = ((Microsoft.Quantum.Simulation.GeneratorIndex -> Microsoft.Quantum.Simulation.EvolutionUnitary));
```

