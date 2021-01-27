---
uid: Microsoft.Quantum.Canon.ApplyOpRepeatedlyOverA
title: Bewerking ApplyOpRepeatedlyOverA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyOpRepeatedlyOverA
qsharp.summary: Applies the same op over a qubit register multiple times.
ms.openlocfilehash: 30e91d8a0292c7389ad83f14e1b7d4a8248cbb96
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841626"
---
# <a name="applyoprepeatedlyovera-operation"></a><span data-ttu-id="37523-102">Bewerking ApplyOpRepeatedlyOverA</span><span class="sxs-lookup"><span data-stu-id="37523-102">ApplyOpRepeatedlyOverA operation</span></span>

<span data-ttu-id="37523-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="37523-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="37523-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="37523-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="37523-105">Past hetzelfde op een Qubit-REGI ster meerdere keren toe.</span><span class="sxs-lookup"><span data-stu-id="37523-105">Applies the same op over a qubit register multiple times.</span></span>

```qsharp
operation ApplyOpRepeatedlyOverA (op : (Qubit[] => Unit is Adj), targets : Int[][], register : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="37523-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="37523-106">Input</span></span>

### <a name="op--qubit--unit--is-adj"></a><span data-ttu-id="37523-107">op: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="37523-107">op : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="37523-108">Een bewerking die meerdere keren wordt toegepast op het Qubit-REGI ster</span><span class="sxs-lookup"><span data-stu-id="37523-108">An operation to be applied multiple times on the qubit register</span></span>


### <a name="targets--int"></a><span data-ttu-id="37523-109">doelen: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="37523-109">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="37523-110">Geneste matrices waarin de doelen van de op-op worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="37523-110">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="37523-111">Elke matrix moet een lijst bevatten met ints die het qubits beschrijven dat moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="37523-111">Each array should contain a list of ints describing the qubits to be used.</span></span>


### <a name="register--qubit"></a><span data-ttu-id="37523-112">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="37523-112">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="37523-113">Qubit-REGI ster waarop moet worden gehandeld.</span><span class="sxs-lookup"><span data-stu-id="37523-113">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="37523-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="37523-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="37523-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="37523-115">See Also</span></span>

- [<span data-ttu-id="37523-116">Micro soft. Quantum. Canon. ApplySeriesOfOps</span><span class="sxs-lookup"><span data-stu-id="37523-116">Microsoft.Quantum.Canon.ApplySeriesOfOps</span></span>](xref:Microsoft.Quantum.Canon.ApplySeriesOfOps)