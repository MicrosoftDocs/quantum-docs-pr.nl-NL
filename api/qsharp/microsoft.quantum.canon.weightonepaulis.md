---
uid: Microsoft.Quantum.Canon.WeightOnePaulis
title: De functie WeightOnePaulis
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: WeightOnePaulis
qsharp.summary: Returns an array of all weight-1 Pauli operators on a given number of qubits.
ms.openlocfilehash: 89802c1bc6f3da8edef27b698eb61098e47dfc85
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703707"
---
# <a name="weightonepaulis-function"></a><span data-ttu-id="80021-102">De functie WeightOnePaulis</span><span class="sxs-lookup"><span data-stu-id="80021-102">WeightOnePaulis function</span></span>

<span data-ttu-id="80021-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="80021-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="80021-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="80021-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="80021-105">Retourneert een matrix van alle Pauli-Opera tors van het gewicht-1 op een gegeven aantal qubits.</span><span class="sxs-lookup"><span data-stu-id="80021-105">Returns an array of all weight-1 Pauli operators on a given number of qubits.</span></span>

```qsharp
function WeightOnePaulis (nQubits : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="80021-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="80021-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="80021-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="80021-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="80021-108">Het aantal qubits waarop de geretourneerde Pauli-Opera tors zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="80021-108">The number of qubits on which the returned Pauli operators are defined.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="80021-109">Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="80021-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="80021-110">Een matrix met multi-Qubit Pauli-Opera Tors, die allemaal worden weer gegeven als een matrix met een lengte `nQubits` .</span><span class="sxs-lookup"><span data-stu-id="80021-110">An array of multi-qubit Pauli operators, each of which is represented as an array with length `nQubits`.</span></span>