---
uid: Microsoft.Quantum.Simulation.IntsToPaulis
title: De functie IntsToPaulis
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Simulation
qsharp.name: IntsToPaulis
qsharp.summary: Converts an array of integers to an array of single-qubit Pauli operators.
ms.openlocfilehash: 6904054bb1aff3a57c80882694b4c217812b2b81
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98842229"
---
# <a name="intstopaulis-function"></a><span data-ttu-id="25571-102">De functie IntsToPaulis</span><span class="sxs-lookup"><span data-stu-id="25571-102">IntsToPaulis function</span></span>

<span data-ttu-id="25571-103">Naam ruimte: [micro soft. Quantum. simulatie](xref:Microsoft.Quantum.Simulation)</span><span class="sxs-lookup"><span data-stu-id="25571-103">Namespace: [Microsoft.Quantum.Simulation](xref:Microsoft.Quantum.Simulation)</span></span>

<span data-ttu-id="25571-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="25571-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="25571-105">Converteert een matrix met gehele getallen naar een matrix van Pauli-Opera tors met één Qubit.</span><span class="sxs-lookup"><span data-stu-id="25571-105">Converts an array of integers to an array of single-qubit Pauli operators.</span></span>

```qsharp
function IntsToPaulis (ints : Int[]) : Pauli[]
```


## <a name="input"></a><span data-ttu-id="25571-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="25571-106">Input</span></span>

### <a name="ints--int"></a><span data-ttu-id="25571-107">ints: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="25571-107">ints : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="25571-108">Matrix van gehele getallen in het bereik `0..3`  dat moet worden geconverteerd naar Pauli-Opera tors.</span><span class="sxs-lookup"><span data-stu-id="25571-108">Array of integers in the range `0..3`  to be converted to Pauli operators.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="25571-109">Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="25571-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="25571-110">Een matrix `paulis` van Pauli-Opera tors `Pauli[]` met dezelfde lengte als `ints` die `paulis[idxPauli]` gelijk is aan het element van `[PauliI, PauliX, PauliY, PauliZ]` gegeven door `ints[idxPauli]` .</span><span class="sxs-lookup"><span data-stu-id="25571-110">An array `paulis` of Pauli operators `Pauli[]` the same length as `ints` such that `paulis[idxPauli]` is equal to the element of `[PauliI, PauliX, PauliY, PauliZ]` given by `ints[idxPauli]`.</span></span>