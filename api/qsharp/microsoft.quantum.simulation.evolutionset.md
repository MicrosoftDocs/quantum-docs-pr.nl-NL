---
uid: Microsoft.Quantum.Simulation.EvolutionSet
title: Door de gebruiker gedefinieerd type ontwikkelings
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: udt
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: EvolutionSet
qsharp.summary: >-
  Represents a set of gates that can be readily implemented and used to implement simulation algorithms.

  Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time
ms.openlocfilehash: 35c0b24da284a5871fd11b6d624102b853b89d19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98856074"
---
# <a name="evolutionset-user-defined-type"></a><span data-ttu-id="1b21a-102">Door de gebruiker gedefinieerd type ontwikkelings</span><span class="sxs-lookup"><span data-stu-id="1b21a-102">EvolutionSet user defined type</span></span>

<span data-ttu-id="1b21a-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="1b21a-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="1b21a-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="1b21a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="1b21a-105">Vertegenwoordigt een set poorten die eenvoudig kunnen worden geïmplementeerd en gebruikt voor het implementeren van simulatie algoritmen.</span><span class="sxs-lookup"><span data-stu-id="1b21a-105">Represents a set of gates that can be readily implemented and used to implement simulation algorithms.</span></span>

<span data-ttu-id="1b21a-106">Elementen in de set worden geïndexeerd door een  <xref:microsoft.quantum.simulation.generatorindex> , en elke set wordt beschreven door een functie van `GeneratorIndex` naar  <xref:microsoft.quantum.simulation.evolutionunitary> , die para meters voor bewerkingen zijn met een reëel getal dat tijd vertegenwoordigt</span><span class="sxs-lookup"><span data-stu-id="1b21a-106">Elements in the set are indexed by a  <xref:microsoft.quantum.simulation.generatorindex>, and each set is described by a function from `GeneratorIndex` to  <xref:microsoft.quantum.simulation.evolutionunitary>, which are operations parameterized by a real number representing time</span></span>

```qsharp

newtype EvolutionSet = ((Microsoft.Quantum.Simulation.GeneratorIndex -> Microsoft.Quantum.Simulation.EvolutionUnitary));
```

