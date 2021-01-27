---
uid: Microsoft.Quantum.Canon.WeightOnePaulis
title: De functie WeightOnePaulis
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: WeightOnePaulis
qsharp.summary: Returns an array of all weight-1 Pauli operators on a given number of qubits.
ms.openlocfilehash: 8aeea795ef5409339e8a1b39c3ffcfaf29d675b6
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98851977"
---
# <a name="weightonepaulis-function"></a><span data-ttu-id="17b92-102">De functie WeightOnePaulis</span><span class="sxs-lookup"><span data-stu-id="17b92-102">WeightOnePaulis function</span></span>

<span data-ttu-id="17b92-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="17b92-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="17b92-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="17b92-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="17b92-105">Retourneert een matrix van alle Pauli-Opera tors van het gewicht-1 op een gegeven aantal qubits.</span><span class="sxs-lookup"><span data-stu-id="17b92-105">Returns an array of all weight-1 Pauli operators on a given number of qubits.</span></span>

```qsharp
function WeightOnePaulis (nQubits : Int) : Pauli[][]
```


## <a name="input"></a><span data-ttu-id="17b92-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="17b92-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="17b92-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="17b92-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="17b92-108">Het aantal qubits waarop de geretourneerde Pauli-Opera tors zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="17b92-108">The number of qubits on which the returned Pauli operators are defined.</span></span>



## <a name="output--pauli"></a><span data-ttu-id="17b92-109">Uitvoer: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[] []</span><span class="sxs-lookup"><span data-stu-id="17b92-109">Output : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[][]</span></span>

<span data-ttu-id="17b92-110">Een matrix met multi-Qubit Pauli-Opera Tors, die allemaal worden weer gegeven als een matrix met een lengte `nQubits` .</span><span class="sxs-lookup"><span data-stu-id="17b92-110">An array of multi-qubit Pauli operators, each of which is represented as an array with length `nQubits`.</span></span>