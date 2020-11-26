---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverA
title: Bewerking ApplyOpRepeatedlyOverA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverA
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 65675a3a83f0ac730b9e3a58f80f77c096c1ce57
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209142"
---
# <a name="applyoprepeatedlyovera-operation"></a><span data-ttu-id="0328d-102">Bewerking ApplyOpRepeatedlyOverA</span><span class="sxs-lookup"><span data-stu-id="0328d-102">ApplyOpRepeatedlyOverA operation</span></span>

<span data-ttu-id="0328d-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="0328d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="0328d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="0328d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="0328d-105">Past hetzelfde op een Qubit-REGI ster meerdere keren toe.</span><span class="sxs-lookup"><span data-stu-id="0328d-105">Applies the same op over a qubit register multiple times.</span></span>

```qsharp
operation ApplyOpRepeatedlyOverA (op : (Qubit[] => Unit is Adj), targets : Int[][], register : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="0328d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="0328d-106">Input</span></span>

### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="0328d-107">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="0328d-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="0328d-108">Een bewerking die meerdere keren wordt toegepast op het Qubit-REGI ster</span><span class="sxs-lookup"><span data-stu-id="0328d-108">An operation to be applied multiple times on the qubit register</span></span>


### <a name="targets--int"></a><span data-ttu-id="0328d-109">doelen: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="0328d-109">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="0328d-110">Geneste matrices waarin de doelen van de op-op worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="0328d-110">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="0328d-111">Elke matrix moet een lijst bevatten met ints die het qubits beschrijven dat moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0328d-111">Each array should contain a list of ints describing the qubits to be used.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="0328d-112">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="0328d-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="0328d-113">Qubit-REGI ster waarop moet worden gehandeld.</span><span class="sxs-lookup"><span data-stu-id="0328d-113">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="0328d-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="0328d-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="0328d-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0328d-115">See Also</span></span>

- [<span data-ttu-id="0328d-116">Micro soft. Quantum. Canon. ApplySeriesOfOps</span><span class="sxs-lookup"><span data-stu-id="0328d-116">Microsoft.Quantum.Canon.ApplySeriesOfOps</span></span>](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)