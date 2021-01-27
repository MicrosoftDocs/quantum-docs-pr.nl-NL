---
uid: Microsoft.Quantum.Simulation.MultiplyGeneratorIndex
title: De functie MultiplyGeneratorIndex
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: MultiplyGeneratorIndex
qsharp.summary: Multiplies the coefficient in a `GeneratorIndex`.
ms.openlocfilehash: b53a483a0c2b8c99b733c9c87289fb212b5ffc89
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848019"
---
# <a name="multiplygeneratorindex-function"></a><span data-ttu-id="8469a-102">De functie MultiplyGeneratorIndex</span><span class="sxs-lookup"><span data-stu-id="8469a-102">MultiplyGeneratorIndex function</span></span>

<span data-ttu-id="8469a-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="8469a-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="8469a-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8469a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8469a-105">Vermenigvuldigt de coëfficiënt in een `GeneratorIndex` .</span><span class="sxs-lookup"><span data-stu-id="8469a-105">Multiplies the coefficient in a `GeneratorIndex`.</span></span>

```qsharp
function MultiplyGeneratorIndex (multiplier : Double, generatorIndex : Microsoft.Quantum.Simulation.GeneratorIndex) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="8469a-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="8469a-106">Input</span></span>

### <a name="multiplier--double"></a><span data-ttu-id="8469a-107">vermenigvuldiger: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8469a-107">multiplier : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8469a-108">De vermenigvuldiger op de coëfficiënt.</span><span class="sxs-lookup"><span data-stu-id="8469a-108">The multiplier on the coefficient.</span></span>


### <a name="generatorindex--generatorindex"></a><span data-ttu-id="8469a-109">generatorIndex: [generatorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="8469a-109">generatorIndex : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="8469a-110">De `GeneratorIndex` te vermenigvuldigen.</span><span class="sxs-lookup"><span data-stu-id="8469a-110">The `GeneratorIndex` to be multiplied.</span></span>



## <a name="output--generatorindex"></a><span data-ttu-id="8469a-111">Uitvoer: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="8469a-111">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>

<span data-ttu-id="8469a-112">Een waarde `GeneratorIndex` die een term met een coëfficiënt heeft die groter is dan een `multiplier` grotere factor.</span><span class="sxs-lookup"><span data-stu-id="8469a-112">A `GeneratorIndex` representing a term with coefficient a factor `multiplier` larger.</span></span>

## <a name="example"></a><span data-ttu-id="8469a-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="8469a-113">Example</span></span>

```qsharp
let gen = GeneratorIndex(([1,2,3],[coeff]),[1,2,3]);
let ((idxPaulis, idxDoubles), idxQubits) = MultiplyGeneratorIndex(multiplier, gen);
// idxDoubles[0] == multiplier * coeff;
```

## <a name="see-also"></a><span data-ttu-id="8469a-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8469a-114">See Also</span></span>

- [<span data-ttu-id="8469a-115">Micro soft. Quantum. simulatie. GeneratorIndex</span><span class="sxs-lookup"><span data-stu-id="8469a-115">Microsoft.Quantum.Simulation.GeneratorIndex</span></span>](xref:Microsoft.Quantum.Simulation.GeneratorIndex)