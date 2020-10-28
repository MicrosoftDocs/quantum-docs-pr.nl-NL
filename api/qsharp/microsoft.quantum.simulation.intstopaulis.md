---
uid: Microsoft.Quantum.Simulation.IntsToPaulis
title: De functie IntsToPaulis
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntsToPaulis
qsharp.summary: Converts an array of integers to an array of single-qubit Pauli operators.
ms.openlocfilehash: 605257aa7ca39e457127e3c3459b5891145b1863
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92701246"
---
# <a name="intstopaulis-function"></a><span data-ttu-id="9c762-102">De functie IntsToPaulis</span><span class="sxs-lookup"><span data-stu-id="9c762-102">IntsToPaulis function</span></span>

<span data-ttu-id="9c762-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="9c762-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="9c762-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9c762-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9c762-105">Converteert een matrix met gehele getallen naar een matrix van Pauli-Opera tors met één Qubit.</span><span class="sxs-lookup"><span data-stu-id="9c762-105">Converts an array of integers to an array of single-qubit Pauli operators.</span></span>

```qsharp
function IntsToPaulis (ints : Int[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="9c762-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9c762-106">Input</span></span>

### <a name="ints--int"></a><span data-ttu-id="9c762-107">ints: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="9c762-107">ints : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="9c762-108">Matrix van gehele getallen in het bereik `0..3`  dat moet worden geconverteerd naar Pauli-Opera tors.</span><span class="sxs-lookup"><span data-stu-id="9c762-108">Array of integers in the range `0..3`  to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="9c762-109">Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="9c762-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="9c762-110">Een matrix `paulis` van Pauli-Opera tors `Pauli[]` met dezelfde lengte als `ints` die `paulis[idxPauli]` gelijk is aan het element van `[PauliI, PauliX, PauliY, PauliZ]` gegeven door `ints[idxPauli]` .</span><span class="sxs-lookup"><span data-stu-id="9c762-110">An array `paulis` of Pauli operators `Pauli[]` the same length as `ints` such that `paulis[idxPauli]` is equal to the element of `[PauliI, PauliX, PauliY, PauliZ]` given by `ints[idxPauli]`.</span></span>