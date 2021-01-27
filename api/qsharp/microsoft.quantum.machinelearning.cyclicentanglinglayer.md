---
uid: Microsoft.Quantum.MachineLearning.CyclicEntanglingLayer
title: De functie CyclicEntanglingLayer
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CyclicEntanglingLayer
qsharp.summary: Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.
ms.openlocfilehash: 5d0af0a60217b69dc7eb8ece8952f2a7f0c09280
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98847388"
---
# <a name="cyclicentanglinglayer-function"></a><span data-ttu-id="2daa5-102">De functie CyclicEntanglingLayer</span><span class="sxs-lookup"><span data-stu-id="2daa5-102">CyclicEntanglingLayer function</span></span>

<span data-ttu-id="2daa5-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="2daa5-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="2daa5-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="2daa5-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="2daa5-105">Retourneert een matrix met op zichzelf staande rotaties langs een bepaalde as, geordend op cyclische basis in een REGI ster van qubits en para meters door afzonderlijke model parameters.</span><span class="sxs-lookup"><span data-stu-id="2daa5-105">Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.</span></span>

```qsharp
function CyclicEntanglingLayer (nQubits : Int, axis : Pauli, stride : Int) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="2daa5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="2daa5-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="2daa5-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2daa5-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2daa5-108">Het aantal qubits dat wordt verwerkt door de opgegeven laag.</span><span class="sxs-lookup"><span data-stu-id="2daa5-108">The number of qubits acted on by the given layer.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="2daa5-109">as: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="2daa5-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="2daa5-110">De rotatieas voor elke draaiing in de opgegeven laag.</span><span class="sxs-lookup"><span data-stu-id="2daa5-110">The rotation axis for each rotation in the given layer.</span></span>


### <a name="stride--int"></a><span data-ttu-id="2daa5-111">Stride: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="2daa5-111">stride : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="2daa5-112">De schei ding tussen de doel-en besturings indexen voor elke draaiing.</span><span class="sxs-lookup"><span data-stu-id="2daa5-112">The separation between the target and control indices for each rotation.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="2daa5-113">Uitvoer: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="2daa5-113">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="2daa5-114">Een matrix van door Qubit beheerde rotaties die cyclisch zijn verdeeld over een REGI ster van `nQubits` qubits.</span><span class="sxs-lookup"><span data-stu-id="2daa5-114">An array of two-qubit controlled rotations laid out cyclically across a register of `nQubits` qubits.</span></span>

## <a name="example"></a><span data-ttu-id="2daa5-115">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="2daa5-115">Example</span></span>

<span data-ttu-id="2daa5-116">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="2daa5-116">The following are equivalent:</span></span>

```qsharp
let layer = CyclicEntanglingLayer(3, PauliX, 2);
let layer = [
    ControlledRotation((0, [2]), PauliX, 0),
    ControlledRotation((1, [0]), PauliX, 1),
    ControlledRotation((2, [1]), PauliX, 2)
];
```