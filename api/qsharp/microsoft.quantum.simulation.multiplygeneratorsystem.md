---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorSystem
title: De functie MultiplyGeneratorSystem
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorSystem
qsharp.summary: Multiplies the coefficient of all terms in a `GeneratorSystem`.
ms.openlocfilehash: effb9e3ca754f77bbe1ea0fb6ca30ae49e92d531
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229151"
---
# <a name="multiplygeneratorsystem-function"></a><span data-ttu-id="22203-102">De functie MultiplyGeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="22203-102">MultiplyGeneratorSystem function</span></span>

<span data-ttu-id="22203-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="22203-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="22203-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="22203-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="22203-105">Vermenigvuldigt de coëfficiënt van alle termen in een `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="22203-105">Multiplies the coefficient of all terms in a `GeneratorSystem`.</span></span>

```qsharp
function MultiplyGeneratorSystem (multiplier : Double, generatorSystem : Microsoft.Quantum.Simulation.GeneratorSystem) : Microsoft.Quantum.Simulation.GeneratorSystem
```


## <a name="input"></a><span data-ttu-id="22203-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="22203-106">Input</span></span>

### <a name="multiplier--double"></a><span data-ttu-id="22203-107">vermenigvuldiger: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="22203-107">multiplier : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="22203-108">De vermenigvuldiger op de coëfficiënt.</span><span class="sxs-lookup"><span data-stu-id="22203-108">The multiplier on the coefficient.</span></span>


### <a name="generatorsystem--generatorsystem"></a><span data-ttu-id="22203-109">generatorSystem: [generatorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="22203-109">generatorSystem : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="22203-110">De `GeneratorSystem` te vermenigvuldigen.</span><span class="sxs-lookup"><span data-stu-id="22203-110">The `GeneratorSystem` to be multiplied.</span></span>



## <a name="output--generatorsystem"></a><span data-ttu-id="22203-111">Uitvoer: [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span><span class="sxs-lookup"><span data-stu-id="22203-111">Output : [GeneratorSystem](xref:Microsoft.Quantum.Simulation.GeneratorSystem)</span></span>

<span data-ttu-id="22203-112">Een `GeneratorSystem` van een systeem met een coëfficiënt die groter is dan een `multiplier` grotere factor.</span><span class="sxs-lookup"><span data-stu-id="22203-112">A `GeneratorSystem` representing a system with coefficients a factor `multiplier` larger.</span></span>

## <a name="see-also"></a><span data-ttu-id="22203-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="22203-113">See Also</span></span>

- [<span data-ttu-id="22203-114">Micro soft. Quantum. simulatie. GeneratorSystem</span><span class="sxs-lookup"><span data-stu-id="22203-114">Microsoft.Quantum.Simulation.GeneratorSystem</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorSystem)