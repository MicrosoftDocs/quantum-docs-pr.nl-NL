---
uid: Microsoft.Quantum.Canon.WeightOnePaulis
title: De functie WeightOnePaulis
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: WeightOnePaulis
qsharp.summary: Returns an array of all weight-1 Pauli operators on a given number of qubits.
ms.openlocfilehash: 904c606393131d51eaa44d464ad52bec509eaf72
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96204535"
---
# <a name="weightonepaulis-function"></a><span data-ttu-id="721a4-102">De functie WeightOnePaulis</span><span class="sxs-lookup"><span data-stu-id="721a4-102">WeightOnePaulis function</span></span>

<span data-ttu-id="721a4-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="721a4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="721a4-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="721a4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="721a4-105">Retourneert een matrix van alle Pauli-Opera tors van het gewicht-1 op een gegeven aantal qubits.</span><span class="sxs-lookup"><span data-stu-id="721a4-105">Returns an array of all weight-1 Pauli operators on a given number of qubits.</span></span>

```qsharp
function WeightOnePaulis (nQubits : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="721a4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="721a4-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="721a4-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="721a4-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="721a4-108">Het aantal qubits waarop de geretourneerde Pauli-Opera tors zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="721a4-108">The number of qubits on which the returned Pauli operators are defined.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="721a4-109">Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="721a4-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="721a4-110">Een matrix met multi-Qubit Pauli-Opera Tors, die allemaal worden weer gegeven als een matrix met een lengte `nQubits` .</span><span class="sxs-lookup"><span data-stu-id="721a4-110">An array of multi-qubit Pauli operators, each of which is represented as an array with length `nQubits`.</span></span>