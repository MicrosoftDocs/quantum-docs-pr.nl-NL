---
uid: Microsoft.Quantum.Simulation.InterpolateGeneratorSystems
title: De functie InterpolateGeneratorSystems
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: InterpolateGeneratorSystems
qsharp.summary: Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.
ms.openlocfilehash: c56f1eaf13afb649777c0d9368e97d85996cc67b
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842269"
---
# <a name="interpolategeneratorsystems-function"></a><span data-ttu-id="b90e3-102">De functie InterpolateGeneratorSystems</span><span class="sxs-lookup"><span data-stu-id="b90e3-102">InterpolateGeneratorSystems function</span></span>

<span data-ttu-id="b90e3-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="b90e3-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="b90e3-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b90e3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b90e3-105">Retourneert een waarde `TimeDependentGeneratorSystem` die de lineaire interpolatie tussen twee `GeneratorSystem` s aangeeft.</span><span class="sxs-lookup"><span data-stu-id="b90e3-105">Returns a `TimeDependentGeneratorSystem` representing the linear interpolation between two `GeneratorSystem`s.</span></span>

```qsharp
function InterpolateGeneratorSystems (generatorSystemStart : Microsoft.Quantum.Simulation.GeneratorSystem, generatorSystemEnd : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem
```


## <a name="input"></a><span data-ttu-id="b90e3-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="b90e3-106">Input</span></span>

### <a name="generatorsystemstart--generatorsystem"></a><span data-ttu-id="b90e3-107">generatorSystemStart: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="b90e3-107">generatorSystemStart : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="b90e3-108">Het begin `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="b90e3-108">The start `GeneratorSystem`.</span></span>


### <a name="generatorsystemend--generatorsystem"></a><span data-ttu-id="b90e3-109">generatorSystemEnd: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="b90e3-109">generatorSystemEnd : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="b90e3-110">Het einde `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="b90e3-110">The end `GeneratorSystem`.</span></span>



## <a name="output--timedependentgeneratorsystem"></a><span data-ttu-id="b90e3-111">Uitvoer: [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="b90e3-111">Output : [TimeDependentGeneratorSystem](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)</span></span>

<span data-ttu-id="b90e3-112">Een `TimeDependentGeneratorSystem` vertegenwoordigt een systeem dat de som is van de invoer Generator systemen, waarbij gewicht $ (1-s) $ op `generatorSystemStart` en gewicht $s $ is ingeschakeld `generatorSystemEnd` .</span><span class="sxs-lookup"><span data-stu-id="b90e3-112">A `TimeDependentGeneratorSystem` representing a system that is the sum of the input generator systems, with weight $(1-s)$ on `generatorSystemStart` and weight $s$ on `generatorSystemEnd`.</span></span>

## <a name="see-also"></a><span data-ttu-id="b90e3-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b90e3-113">See Also</span></span>

- [<span data-ttu-id="b90e3-114">Micro soft. Quantum. simulatie. GeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="b90e3-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)
- [<span data-ttu-id="b90e3-115">Micro soft. Quantum. simulatie. TimeDependentGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="b90e3-115">Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.TimeDependentGeneratorSystem)