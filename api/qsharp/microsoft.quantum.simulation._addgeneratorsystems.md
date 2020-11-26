---
uid: Microsoft.Quantum.Simulation._AddGeneratorSystems
title: Functie _AddGeneratorSystems
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: _AddGeneratorSystems
qsharp.summary: Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.
ms.openlocfilehash: ffb635d7cb6c388c2158b7adb6bb872b0c77cdb1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96229746"
---
# <a name="_addgeneratorsystems-function"></a><span data-ttu-id="c6084-102">Functie _AddGeneratorSystems</span><span class="sxs-lookup"><span data-stu-id="c6084-102">_AddGeneratorSystems function</span></span>

<span data-ttu-id="c6084-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="c6084-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="c6084-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c6084-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c6084-105">Voegt twee `GeneratorSystem` s toe om een nieuwe te maken `GeneratorSystem` .</span><span class="sxs-lookup"><span data-stu-id="c6084-105">Adds two `GeneratorSystem`s to create a new `GeneratorSystem`.</span></span>

```qsharp
function _AddGeneratorSystems (idxTerm : Int, nTermsA : Int, nTermsB : Int, generatorIndexFunctionA : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex), generatorIndexFunctionB : (Int -> Microsoft.Quantum.Simulation.GeneratorIndex)) : Microsoft.Quantum.Simulation.GeneratorIndex
```


## <a name="input"></a><span data-ttu-id="c6084-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c6084-106">Input</span></span>

### <a name="idxterm--int"></a><span data-ttu-id="c6084-107">idxTerm: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c6084-107">idxTerm : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="ntermsa--int"></a><span data-ttu-id="c6084-108">nTermsA: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c6084-108">nTermsA : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="ntermsb--int"></a><span data-ttu-id="c6084-109">nTermsB: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c6084-109">nTermsB : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="generatorindexfunctiona--int---generatorindex"></a><span data-ttu-id="c6084-110">generatorIndexFunctionA: [int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="c6084-110">generatorIndexFunctionA : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>




### <a name="generatorindexfunctionb--int---generatorindex"></a><span data-ttu-id="c6084-111">generatorIndexFunctionB: [int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="c6084-111">generatorIndexFunctionB : [Int](xref:microsoft.quantum.lang-ref.int) -> [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>





## <a name="output--generatorindex"></a><span data-ttu-id="c6084-112">Uitvoer: [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span><span class="sxs-lookup"><span data-stu-id="c6084-112">Output : [GeneratorIndex](xref:Microsoft.Quantum.Simulation.GeneratorIndex)</span></span>



## <a name="remarks"></a><span data-ttu-id="c6084-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c6084-113">Remarks</span></span>

<span data-ttu-id="c6084-114">Dit is een tussen stap en mag niet worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="c6084-114">This is an intermediate step and should not be called.</span></span>