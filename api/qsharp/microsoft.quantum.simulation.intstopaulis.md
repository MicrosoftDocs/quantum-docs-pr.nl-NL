---
uid: Microsoft.Quantum.Simulation.IntsToPaulis
title: De functie IntsToPaulis
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntsToPaulis
qsharp.summary: Converts an array of integers to an array of single-qubit Pauli operators.
ms.openlocfilehash: 2333dcbd2988480e2b2b9b217b26705f3578de00
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96230528"
---
# <a name="intstopaulis-function"></a><span data-ttu-id="4d504-102">De functie IntsToPaulis</span><span class="sxs-lookup"><span data-stu-id="4d504-102">IntsToPaulis function</span></span>

<span data-ttu-id="4d504-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="4d504-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="4d504-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="4d504-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="4d504-105">Converteert een matrix met gehele getallen naar een matrix van Pauli-Opera tors met één Qubit.</span><span class="sxs-lookup"><span data-stu-id="4d504-105">Converts an array of integers to an array of single-qubit Pauli operators.</span></span>

```qsharp
function IntsToPaulis (ints : Int[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="4d504-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="4d504-106">Input</span></span>

### <a name="ints--int"></a><span data-ttu-id="4d504-107">ints: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="4d504-107">ints : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="4d504-108">Matrix van gehele getallen in het bereik `0..3`  dat moet worden geconverteerd naar Pauli-Opera tors.</span><span class="sxs-lookup"><span data-stu-id="4d504-108">Array of integers in the range `0..3`  to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="4d504-109">Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="4d504-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="4d504-110">Een matrix `paulis` van Pauli-Opera tors `Pauli[]` met dezelfde lengte als `ints` die `paulis[idxPauli]` gelijk is aan het element van `[PauliI, PauliX, PauliY, PauliZ]` gegeven door `ints[idxPauli]` .</span><span class="sxs-lookup"><span data-stu-id="4d504-110">An array `paulis` of Pauli operators `Pauli[]` the same length as `ints` such that `paulis[idxPauli]` is equal to the element of `[PauliI, PauliX, PauliY, PauliZ]` given by `ints[idxPauli]`.</span></span>