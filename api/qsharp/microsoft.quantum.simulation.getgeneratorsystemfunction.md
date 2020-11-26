---
uid: Microsoft.Quantum.Simulation.GetGeneratorSystemFunction
title: De functie GetGeneratorSystemFunction
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: GetGeneratorSystemFunction
qsharp.summary: Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.
ms.openlocfilehash: 28e3c12d0ae0b08fc368c25eeb6f38d2834ca912
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229304"
---
# <a name="getgeneratorsystemfunction-function"></a><span data-ttu-id="634dc-102">De functie GetGeneratorSystemFunction</span><span class="sxs-lookup"><span data-stu-id="634dc-102">GetGeneratorSystemFunction function</span></span>

<span data-ttu-id="634dc-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="634dc-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="634dc-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="634dc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="634dc-105">Haalt de `GeneratorIndex` functie op in een `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="634dc-105">Retrieves the `GeneratorIndex` function in a `GeneratorSystem`.</span></span>

```qsharp
function GetGeneratorSystemFunction (generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)
```


## <a name="input"></a><span data-ttu-id="634dc-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="634dc-106">Input</span></span>

### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="634dc-107">generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="634dc-107">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="634dc-108">Het is `GeneratorSystem` van belang.</span><span class="sxs-lookup"><span data-stu-id="634dc-108">The `GeneratorSystem` of interest.</span></span>



## <a name="output--int---generatorindex"></a><span data-ttu-id="634dc-109">Uitvoer: [int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="634dc-109">Output : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="634dc-110">Een functie waarmee elke `GeneratorIndex` term in een Hamiltonian wordt geïndexeerd.</span><span class="sxs-lookup"><span data-stu-id="634dc-110">An function that indexes each `GeneratorIndex` term in a Hamiltonian.</span></span>

## <a name="see-also"></a><span data-ttu-id="634dc-111">Zie ook</span><span class="sxs-lookup"><span data-stu-id="634dc-111">See Also</span></span>

- [<span data-ttu-id="634dc-112">Micro soft. Quantum. simulatie. GeneratorIndex</span><span class="sxs-lookup"><span data-stu-id="634dc-112">Microsoft.Quantum.Simulation.GeneratorIndex</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorIndex)
- [<span data-ttu-id="634dc-113">Micro soft. Quantum. simulatie. GeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="634dc-113">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)