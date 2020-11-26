---
uid: Microsoft.Quantum.Simulation.EvolutionSet
title: Door de gebruiker gedefinieerd type ontwikkelings
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionSet
qsharp.summary: >-
  Represents a set of gates that can be readily implemented and used to implement simulation algorithms.

  Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time
ms.openlocfilehash: ee8f3c0716f035dcb0c4fad557092fbf8dd3c356
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229406"
---
# <a name="evolutionset-user-defined-type"></a><span data-ttu-id="fb37c-102">Door de gebruiker gedefinieerd type ontwikkelings</span><span class="sxs-lookup"><span data-stu-id="fb37c-102">EvolutionSet user defined type</span></span>

<span data-ttu-id="fb37c-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="fb37c-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="fb37c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fb37c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fb37c-105">Vertegenwoordigt een set poorten die eenvoudig kunnen worden geïmplementeerd en gebruikt voor het implementeren van simulatie algoritmen.</span><span class="sxs-lookup"><span data-stu-id="fb37c-105">Represents a set of gates that can be readily implemented and used to implement simulation algorithms.</span></span>

<span data-ttu-id="fb37c-106">Elementen in de set worden geïndexeerd door een  <xref:microsoft.quantum.simulation.generatorindex> , en elke set wordt beschreven door een functie van `GeneratorIndex` naar  <xref:microsoft.quantum.simulation.evolutionunitary> , die para meters voor bewerkingen zijn met een reëel getal dat tijd vertegenwoordigt</span><span class="sxs-lookup"><span data-stu-id="fb37c-106">Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time</span></span>

```qsharp

newtype EvolutionSet = ((Microsoft.Quantum.Simulation.GeneratorIndex -> Microsoft.Quantum.Simulation.EvolutionUnitary));
```

