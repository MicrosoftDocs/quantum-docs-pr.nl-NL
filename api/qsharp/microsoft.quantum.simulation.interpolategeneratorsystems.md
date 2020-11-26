---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystems
title: De functie InterpolateGeneratorSystems
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystems
qsharp.summary: Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.
ms.openlocfilehash: ee47637996313fe1b77c76f00b08417dac956247
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230579"
---
# <a name="interpolategeneratorsystems-function"></a><span data-ttu-id="5f87d-102">De functie InterpolateGeneratorSystems</span><span class="sxs-lookup"><span data-stu-id="5f87d-102">InterpolateGeneratorSystems function</span></span>

<span data-ttu-id="5f87d-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="5f87d-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="5f87d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5f87d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5f87d-105">Retourneert een waarde `TimeDependentGeneratorSystem` die de lineaire interpolatie tussen twee `GeneratorSystem` s aangeeft.</span><span class="sxs-lookup"><span data-stu-id="5f87d-105">Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.</span></span>

```qsharp
function InterpolateGeneratorSystems (generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
```


## <a name="input"></a><span data-ttu-id="5f87d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="5f87d-106">Input</span></span>

### <a name="generatorsystemstart--generatorsystem"></a><span data-ttu-id="5f87d-107">generatorSystemStart: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="5f87d-107">generatorSystemStart : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="5f87d-108">Het begin `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="5f87d-108">The start `GeneratorSystem`.</span></span>


### <a name="generatorsystemend--generatorsystem"></a><span data-ttu-id="5f87d-109">generatorSystemEnd: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="5f87d-109">generatorSystemEnd : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="5f87d-110">Het einde `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="5f87d-110">The end `GeneratorSystem`.</span></span>



## <a name="output--timedependentgeneratorsystem"></a><span data-ttu-id="5f87d-111">Uitvoer: [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="5f87d-111">Output : [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span></span>

<span data-ttu-id="5f87d-112">Een `TimeDependentGeneratorSystem` vertegenwoordigt een systeem dat de som is van de invoer Generator systemen, waarbij gewicht $ (1-s) $ op `generatorSystemStart` en gewicht $s $ is ingeschakeld `generatorSystemEnd` .</span><span class="sxs-lookup"><span data-stu-id="5f87d-112">A `TimeDependentGeneratorSystem` representing a system that is the sum of the input generator systems, with weight $(1-s)$ on `generatorSystemStart` and weight $s$ on `generatorSystemEnd`.</span></span>

## <a name="see-also"></a><span data-ttu-id="5f87d-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5f87d-113">See Also</span></span>

- [<span data-ttu-id="5f87d-114">Micro soft. Quantum. simulatie. GeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="5f87d-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
- [<span data-ttu-id="5f87d-115">Micro soft. Quantum. simulatie. TimeDependentGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="5f87d-115">Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)