---
uid: Microsoft.Quantum.MachineLearning.LocalRotationsLayer
title: De functie LocalRotationsLayer
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: LocalRotationsLayer
qsharp.summary: Returns an array of uncontrolled (single-qubit) rotations along a given axis, with one rotation for each qubit in a register, parameterized by distinct model parameters.
ms.openlocfilehash: 1549f24427f19bacbadf72e00c1c0181b64bcb73
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96211726"
---
# <a name="localrotationslayer-function"></a><span data-ttu-id="679a7-102">De functie LocalRotationsLayer</span><span class="sxs-lookup"><span data-stu-id="679a7-102">LocalRotationsLayer function</span></span>

<span data-ttu-id="679a7-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="679a7-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="679a7-104">Pakket: [micro soft. Quantum. MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="679a7-104">Package: [Microsoft.Quantum.MachineLearning](https://nuget.org/packages/Microsoft.Quantum.MachineLearning)</span></span>


<span data-ttu-id="679a7-105">Retourneert een matrix met onbeheerde rotaties op een bepaalde as, met één rotatie voor elke qubit in een REGI ster, para meters door afzonderlijke model parameters.</span><span class="sxs-lookup"><span data-stu-id="679a7-105">Returns an array of uncontrolled (single-qubit) rotations along a given axis, with one rotation for each qubit in a register, parameterized by distinct model parameters.</span></span>

```qsharp
function LocalRotationsLayer (nQubits : Int, axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="679a7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="679a7-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="679a7-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="679a7-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="679a7-108">Het aantal qubits dat wordt verwerkt door de opgegeven laag.</span><span class="sxs-lookup"><span data-stu-id="679a7-108">The number of qubits acted on by the given layer.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="679a7-109">as: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="679a7-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="679a7-110">De rotatieas voor elke draaiing in de opgegeven laag.</span><span class="sxs-lookup"><span data-stu-id="679a7-110">The rotation axis for each rotation in the given layer.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="679a7-111">Uitvoer: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="679a7-111">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="679a7-112">Een matrix met beheerde rotaties over de opgegeven as, één op elk van de `nQubits` qubits.</span><span class="sxs-lookup"><span data-stu-id="679a7-112">An array of controlled rotations about the given axis, one on each of `nQubits` qubits.</span></span>