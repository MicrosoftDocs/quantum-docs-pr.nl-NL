---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOps
title: Bewerking ApplySeriesOfOps
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOps
qsharp.summary: Applies a list of ops and their targets sequentially on an array.
ms.openlocfilehash: b086b01b0be86bd25a6d6cdef26bfbb53e484cb2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841503"
---
# <a name="applyseriesofops-operation"></a><span data-ttu-id="71486-102">Bewerking ApplySeriesOfOps</span><span class="sxs-lookup"><span data-stu-id="71486-102">ApplySeriesOfOps operation</span></span>

<span data-ttu-id="71486-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="71486-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="71486-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="71486-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="71486-105">Past een lijst van OPS en hun doelen opeenvolgend toe op een matrix.</span><span class="sxs-lookup"><span data-stu-id="71486-105">Applies a list of ops and their targets sequentially on an array.</span></span>

```qsharp
operation ApplySeriesOfOps<'T> (listOfOps : ('T[] => Unit)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="71486-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="71486-106">Input</span></span>

### <a name="listofops--t--unit-"></a><span data-ttu-id="71486-107">listOfOps: 'T [] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="71486-107">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) []</span></span>

<span data-ttu-id="71486-108">De lijst met bewerkingen, waarbij elke matrix wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="71486-108">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="71486-109">Ze worden eerst opeenvolgend en laagste index toegepast.</span><span class="sxs-lookup"><span data-stu-id="71486-109">They are applied sequentially, lowest index first.</span></span>


### <a name="targets--int"></a><span data-ttu-id="71486-110">doelen: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="71486-110">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="71486-111">Geneste matrices waarin de doelen van de op-op worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="71486-111">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="71486-112">Elke matrix moet een lijst met ints bevatten waarin de indexen worden beschreven die moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="71486-112">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="71486-113">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="71486-113">register : 'T[]</span></span>

<span data-ttu-id="71486-114">Qubit-REGI ster waarop moet worden gehandeld.</span><span class="sxs-lookup"><span data-stu-id="71486-114">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="71486-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="71486-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="71486-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="71486-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="71486-117">T</span><span class="sxs-lookup"><span data-stu-id="71486-117">'T</span></span>



## <a name="example"></a><span data-ttu-id="71486-118">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="71486-118">Example</span></span>

<span data-ttu-id="71486-119">Het volgende is van toepassing exp ([PauliX, PauliY], 0,5) op qubits 0, 1//X tot Qubit 2 toestaan OPS = [exp ([PauliX, PauliY], 0,5, _), ApplyToFirstQubit (X, _)]; indices = [[0, 1], [2]]; ApplySeriesOfOps (OPS, indices, qubitArray);</span><span class="sxs-lookup"><span data-stu-id="71486-119">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubit(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOps(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="71486-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="71486-120">See Also</span></span>

- [<span data-ttu-id="71486-121">Micro soft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="71486-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)