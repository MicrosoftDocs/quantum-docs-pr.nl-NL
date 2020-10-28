---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystems
title: De functie InterpolateGeneratorSystems
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystems
qsharp.summary: Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.
ms.openlocfilehash: 9881c27577023dafff0bfc6d961877db44fec0eb
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701721"
---
# <a name="interpolategeneratorsystems-function"></a><span data-ttu-id="48ad7-102">De functie InterpolateGeneratorSystems</span><span class="sxs-lookup"><span data-stu-id="48ad7-102">InterpolateGeneratorSystems function</span></span>

<span data-ttu-id="48ad7-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="48ad7-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="48ad7-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="48ad7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="48ad7-105">Retourneert een waarde `TimeDependentGeneratorSystem` die de lineaire interpolatie tussen twee `GeneratorSystem` s aangeeft.</span><span class="sxs-lookup"><span data-stu-id="48ad7-105">Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.</span></span>

```qsharp
function InterpolateGeneratorSystems (generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
```


## <a name="input"></a><span data-ttu-id="48ad7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="48ad7-106">Input</span></span>

### <a name="generatorsystemstart--generatorsystem"></a><span data-ttu-id="48ad7-107">generatorSystemStart: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="48ad7-107">generatorSystemStart : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="48ad7-108">Het begin `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="48ad7-108">The start `GeneratorSystem`.</span></span>


### <a name="generatorsystemend--generatorsystem"></a><span data-ttu-id="48ad7-109">generatorSystemEnd: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="48ad7-109">generatorSystemEnd : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="48ad7-110">Het einde `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="48ad7-110">The end `GeneratorSystem`.</span></span>



## <a name="output--timedependentgeneratorsystem"></a><span data-ttu-id="48ad7-111">Uitvoer: [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="48ad7-111">Output : [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span></span>

<span data-ttu-id="48ad7-112">Een `TimeDependentGeneratorSystem` vertegenwoordigt een systeem dat de som is van de invoer Generator systemen, waarbij gewicht $ (1-s) $ op `generatorSystemStart` en gewicht $s $ is ingeschakeld `generatorSystemEnd` .</span><span class="sxs-lookup"><span data-stu-id="48ad7-112">A `TimeDependentGeneratorSystem` representing a system that is the sum of the input generator systems, with weight $(1-s)$ on `generatorSystemStart` and weight $s$ on `generatorSystemEnd`.</span></span>

## <a name="see-also"></a><span data-ttu-id="48ad7-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="48ad7-113">See Also</span></span>

- [<span data-ttu-id="48ad7-114">Micro soft. Quantum. simulatie. GeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="48ad7-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
- [<span data-ttu-id="48ad7-115">Micro soft. Quantum. simulatie. TimeDependentGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="48ad7-115">Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)