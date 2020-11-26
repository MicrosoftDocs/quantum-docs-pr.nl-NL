---
uid: Microsoft.Quantum.Chemistry.JordanWigner.JordanWignerFermionFunction
title: De functie JordanWignerFermionFunction
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Chemistry.JordanWigner
qsharp.name: JordanWignerFermionFunction
qsharp.summary: Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.
ms.openlocfilehash: e1eeed0dcd4084401e2680ff1188db4225ee85ca
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96214752"
---
# <a name="jordanwignerfermionfunction-function"></a><span data-ttu-id="e7718-102">De functie JordanWignerFermionFunction</span><span class="sxs-lookup"><span data-stu-id="e7718-102">JordanWignerFermionFunction function</span></span>

<span data-ttu-id="e7718-103">Naam ruimte: [micro soft. Quantum. chemie. JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span><span class="sxs-lookup"><span data-stu-id="e7718-103">Namespace: [Microsoft.Quantum.Chemistry.JordanWigner](xref:Microsoft.Quantum.Chemistry.JordanWigner)</span></span>

<span data-ttu-id="e7718-104">Pakket: [micro soft. Quantum. chemie](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span><span class="sxs-lookup"><span data-stu-id="e7718-104">Package: [Microsoft.Quantum.Chemistry](https://nuget.org/packages/Microsoft.Quantum.Chemistry)</span></span>


<span data-ttu-id="e7718-105">Dit object vertegenwoordigt een dynamische generator als een set simulatieve Gates en een uitbrei ding in de JordanWigner basis.</span><span class="sxs-lookup"><span data-stu-id="e7718-105">Represents a dynamical generator as a set of simulatable gates and an expansion in the JordanWigner basis.</span></span>

```qsharp
function JordanWignerFermionFunction (generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.EvolutionUnitary
```


## <a name="input"></a><span data-ttu-id="e7718-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e7718-106">Input</span></span>

### <a name="generatorindex--generatorindex"></a><span data-ttu-id="e7718-107">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="e7718-107">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="e7718-108">Een generator index die wordt weer gegeven als unitary-ontwikkeling in de JordanWigner.</span><span class="sxs-lookup"><span data-stu-id="e7718-108">A generator index to be represented as unitary evolution in the JordanWigner.</span></span>



## <a name="output--evolutionunitary"></a><span data-ttu-id="e7718-109">Uitvoer: [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span><span class="sxs-lookup"><span data-stu-id="e7718-109">Output : [EvolutionUnitary](xref:Microsoft.Quantum.Simulation.EvolutionUnitary)</span></span>

<span data-ttu-id="e7718-110">Een `EvolutionUnitary` representatieve tijd ontwikkeling op basis van de term waarnaar wordt verwezen in generatorIndex.</span><span class="sxs-lookup"><span data-stu-id="e7718-110">An `EvolutionUnitary` representing time-evolution by the term referenced in \`generatorIndex.</span></span>