---
uid: Microsoft.Quantum.Canon.PermuteQubits
title: Bewerking PermuteQubits
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: PermuteQubits
qsharp.summary: Permutes qubits by using the SWAP operation.
ms.openlocfilehash: 0f4d8819d5b08f4d5370f8fdc407b2eb2a3e5f21
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703905"
---
# <a name="permutequbits-operation"></a><span data-ttu-id="d19b2-102">Bewerking PermuteQubits</span><span class="sxs-lookup"><span data-stu-id="d19b2-102">PermuteQubits operation</span></span>

<span data-ttu-id="d19b2-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d19b2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d19b2-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d19b2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d19b2-105">Permutaties qubits met behulp van de wissel bewerking.</span><span class="sxs-lookup"><span data-stu-id="d19b2-105">Permutes qubits by using the SWAP operation.</span></span>

```qsharp
operation PermuteQubits (ordering : Int[], register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d19b2-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d19b2-106">Input</span></span>

### <a name="ordering--int"></a><span data-ttu-id="d19b2-107">Volg orde: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="d19b2-107">ordering : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="d19b2-108">Hierin wordt de nieuwe volg orde van de qubits beschreven, waarbij de Qubit bij index i nu bij de volg orde [i] komt.</span><span class="sxs-lookup"><span data-stu-id="d19b2-108">Describes the new ordering of the qubits, where the qubit at index i will now be at ordering[i].</span></span>


### <a name="register--qubit"></a><span data-ttu-id="d19b2-109">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d19b2-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d19b2-110">Qubit-REGI ster waarop moet worden gehandeld.</span><span class="sxs-lookup"><span data-stu-id="d19b2-110">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d19b2-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d19b2-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

