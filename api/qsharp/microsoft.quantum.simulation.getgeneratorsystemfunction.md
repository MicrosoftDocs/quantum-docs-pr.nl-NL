---
uid: Microsoft.Quantum.Simulation.GetGeneratorSystemFunction
title: De functie GetGeneratorSystemFunction
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GetGeneratorSystemFunction
qsharp.summary: Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.
ms.openlocfilehash: 60ebbdbd1020d41a54426377043fc0c84ceec504
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92708887"
---
# <a name="getgeneratorsystemfunction-function"></a><span data-ttu-id="60f53-102">De functie GetGeneratorSystemFunction</span><span class="sxs-lookup"><span data-stu-id="60f53-102">GetGeneratorSystemFunction function</span></span>

<span data-ttu-id="60f53-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="60f53-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="60f53-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="60f53-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="60f53-105">Haalt de `GeneratorIndex` functie op in een `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="60f53-105">Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.</span></span>

```qsharp
function GetGeneratorSystemFunction (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)
```


## <a name="input"></a><span data-ttu-id="60f53-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="60f53-106">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="60f53-107">generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="60f53-107">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="60f53-108">Het is `GeneratorSystem` van belang.</span><span class="sxs-lookup"><span data-stu-id="60f53-108">The `GeneratorSystem` of interest.</span></span>



## <a name="output--int---generatorindex"></a><span data-ttu-id="60f53-109">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="60f53-109">Output : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="60f53-110">Een functie waarmee elke `GeneratorIndex` term in een Hamiltonian wordt geïndexeerd.</span><span class="sxs-lookup"><span data-stu-id="60f53-110">An function that indexes each `GeneratorIndex` term in a Hamiltonian.</span></span>

## <a name="see-also"></a><span data-ttu-id="60f53-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="60f53-111">See Also</span></span>

- [<span data-ttu-id="60f53-112">Micro soft. Quantum. simulatie. GeneratorIndex</span><span class="sxs-lookup"><span data-stu-id="60f53-112">Microsoft.Quantum.Simulation.GeneratorIndex</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorIndex)
- [<span data-ttu-id="60f53-113">Micro soft. Quantum. simulatie. GeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="60f53-113">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)