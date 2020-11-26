---
uid: Microsoft.Quantum.MachineLearning.CyclicEntanglingLayer
title: De functie CyclicEntanglingLayer
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: CyclicEntanglingLayer
qsharp.summary: Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.
ms.openlocfilehash: 5421765e36ef3e8e744e118206dafcb2bb582cc2
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211930"
---
# <a name="cyclicentanglinglayer-function"></a><span data-ttu-id="c993d-102">De functie CyclicEntanglingLayer</span><span class="sxs-lookup"><span data-stu-id="c993d-102">CyclicEntanglingLayer function</span></span>

<span data-ttu-id="c993d-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="c993d-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="c993d-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="c993d-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="c993d-105">Retourneert een matrix met op zichzelf staande rotaties langs een bepaalde as, geordend op cyclische basis in een REGI ster van qubits en para meters door afzonderlijke model parameters.</span><span class="sxs-lookup"><span data-stu-id="c993d-105">Returns an array of singly controlled rotations along a given axis, arranged cyclically across a register of qubits, and parameterized by distinct model parameters.</span></span>

```qsharp
function CyclicEntanglingLayer (nQubits : Int, axis : Pauli, stride : Int) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="c993d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c993d-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="c993d-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c993d-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c993d-108">Het aantal qubits dat wordt verwerkt door de opgegeven laag.</span><span class="sxs-lookup"><span data-stu-id="c993d-108">The number of qubits acted on by the given layer.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="c993d-109">as: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="c993d-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="c993d-110">De rotatieas voor elke draaiing in de opgegeven laag.</span><span class="sxs-lookup"><span data-stu-id="c993d-110">The rotation axis for each rotation in the given layer.</span></span>


### <a name="stride--int"></a><span data-ttu-id="c993d-111">Stride: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c993d-111">stride : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c993d-112">De schei ding tussen de doel-en besturings indexen voor elke draaiing.</span><span class="sxs-lookup"><span data-stu-id="c993d-112">The separation between the target and control indices for each rotation.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="c993d-113">Uitvoer: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="c993d-113">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="c993d-114">Een matrix van door Qubit beheerde rotaties die cyclisch zijn verdeeld over een REGI ster van `nQubits` qubits.</span><span class="sxs-lookup"><span data-stu-id="c993d-114">An array of two-qubit controlled rotations laid out cyclically across a register of `nQubits` qubits.</span></span>