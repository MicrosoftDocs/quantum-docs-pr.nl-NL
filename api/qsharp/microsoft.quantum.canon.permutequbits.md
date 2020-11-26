---
uid: Microsoft.Quantum.Canon.PermuteQubits
title: Bewerking PermuteQubits
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: PermuteQubits
qsharp.summary: Permutes qubits by using the SWAP operation.
ms.openlocfilehash: deb5fa5b0bc0509c957e01bf22e491ad3e2214f3
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205599"
---
# <a name="permutequbits-operation"></a><span data-ttu-id="cbe0b-102">Bewerking PermuteQubits</span><span class="sxs-lookup"><span data-stu-id="cbe0b-102">PermuteQubits operation</span></span>

<span data-ttu-id="cbe0b-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cbe0b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cbe0b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cbe0b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cbe0b-105">Permutaties qubits met behulp van de wissel bewerking.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-105">Permutes qubits by using the SWAP operation.</span></span>

```qsharp
operation PermuteQubits (ordering : Int[], register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="cbe0b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="cbe0b-106">Input</span></span>

### <a name="ordering--int"></a><span data-ttu-id="cbe0b-107">Volg orde: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="cbe0b-107">ordering : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="cbe0b-108">Hierin wordt de nieuwe volg orde van de qubits beschreven, waarbij de Qubit bij index i nu bij de volg orde [i] komt.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-108">Describes the new ordering of the qubits, where the qubit at index i will now be at ordering[i].</span></span>


### <a name="register--qubit"></a><span data-ttu-id="cbe0b-109">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="cbe0b-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="cbe0b-110">Qubit-REGI ster waarop moet worden gehandeld.</span><span class="sxs-lookup"><span data-stu-id="cbe0b-110">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cbe0b-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cbe0b-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

