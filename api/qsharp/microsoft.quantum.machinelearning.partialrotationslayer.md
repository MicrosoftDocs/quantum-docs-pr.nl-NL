---
uid: Microsoft.Quantum.MachineLearning.PartialRotationsLayer
title: De functie PartialRotationsLayer
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.MachineLearning
qsharp.name: PartialRotationsLayer
qsharp.summary: Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.
ms.openlocfilehash: ab964d2c43a13a5daf64aefdeccd1c26cd371ff4
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707980"
---
# <a name="partialrotationslayer-function"></a><span data-ttu-id="ccb10-102">De functie PartialRotationsLayer</span><span class="sxs-lookup"><span data-stu-id="ccb10-102">PartialRotationsLayer function</span></span>

<span data-ttu-id="ccb10-103">Naam ruimte: [micro soft. Quantum. MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span><span class="sxs-lookup"><span data-stu-id="ccb10-103">Namespace: [Microsoft.Quantum.MachineLearning](xref:Microsoft.Quantum.MachineLearning)</span></span>

<span data-ttu-id="ccb10-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="ccb10-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="ccb10-105">Retourneert een matrix met enkelvoudige draaiing langs een bepaalde as, para meters door afzonderlijke model parameters.</span><span class="sxs-lookup"><span data-stu-id="ccb10-105">Returns an array of single-qubit rotations along a given axis, parameterized by distinct model parameters.</span></span>

```qsharp
function PartialRotationsLayer (idxsQubits : Int[], axis : Pauli) : Microsoft.Quantum.MachineLearning.ControlledRotation[]
```


## <a name="input"></a><span data-ttu-id="ccb10-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="ccb10-106">Input</span></span>

### <a name="idxsqubits--int"></a><span data-ttu-id="ccb10-107">idxsQubits: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ccb10-107">idxsQubits : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ccb10-108">Indexen voor de qubits die moeten worden gebruikt als de doelen voor elke draaiing.</span><span class="sxs-lookup"><span data-stu-id="ccb10-108">Indices for the qubits to be used as the targets for each rotation.</span></span>


### <a name="axis--pauli"></a><span data-ttu-id="ccb10-109">as: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="ccb10-109">axis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="ccb10-110">De rotatieas voor elke draaiing in de opgegeven laag.</span><span class="sxs-lookup"><span data-stu-id="ccb10-110">The rotation axis for each rotation in the given layer.</span></span>



## <a name="output--controlledrotation"></a><span data-ttu-id="ccb10-111">Uitvoer: [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span><span class="sxs-lookup"><span data-stu-id="ccb10-111">Output : [ControlledRotation](xref:Microsoft.Quantum.MachineLearning.ControlledRotation)[]</span></span>

<span data-ttu-id="ccb10-112">Een matrix met beheerde rotaties over de opgegeven as, één op elk van de `nQubits` qubits.</span><span class="sxs-lookup"><span data-stu-id="ccb10-112">An array of controlled rotations about the given axis, one on each of `nQubits` qubits.</span></span>