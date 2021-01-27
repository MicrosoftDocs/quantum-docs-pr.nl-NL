---
uid: Microsoft.Quantum.MachineLearning.PartialRotationsLayer
title: De functie PartialRotationsLayer
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: PartialRotationsLayer
qsharp.summary: Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.
ms.openlocfilehash: e230df9b28c59e1d532d5b36adf90efa01f0f33e
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852924"
---
# <a name="partialrotationslayer-function"></a><span data-ttu-id="79f04-102">De functie PartialRotationsLayer</span><span class="sxs-lookup"><span data-stu-id="79f04-102">PartialRotationsLayer function</span></span>

<span data-ttu-id="79f04-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="79f04-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="79f04-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="79f04-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="79f04-105">Retourneert een matrix met enkelvoudige draaiing langs een bepaalde as, para meters door afzonderlijke model parameters.</span><span class="sxs-lookup"><span data-stu-id="79f04-105">Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.</span></span>

```qsharp
function PartialRotationsLayer (idxsQubits : Int[], axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="79f04-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="79f04-106">Input</span></span>

### <a name="idxsqubits--int"></a><span data-ttu-id="79f04-107">idxsQubits: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="79f04-107">idxsQubits : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="79f04-108">Indexen voor de qubits die moeten worden gebruikt als de doelen voor elke draaiing.</span><span class="sxs-lookup"><span data-stu-id="79f04-108">Indices for the qubits to be used as the targets for each rotation.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="79f04-109">as: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="79f04-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="79f04-110">De rotatieas voor elke draaiing in de opgegeven laag.</span><span class="sxs-lookup"><span data-stu-id="79f04-110">The rotation axis for each rotation in the given layer.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="79f04-111">Uitvoer: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="79f04-111">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="79f04-112">Een matrix met beheerde rotaties over de opgegeven as, één op elk van de `nQubits` qubits.</span><span class="sxs-lookup"><span data-stu-id="79f04-112">An array of controlled rotations about the given axis, one on each of `nQubits` qubits.</span></span>