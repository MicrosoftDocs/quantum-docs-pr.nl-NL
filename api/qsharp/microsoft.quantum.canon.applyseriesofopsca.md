---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: Bewerking ApplySeriesOfOpsCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 9a1f6189428b086c38b1d0f289afb18c2cf1be40
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850873"
---
# <a name="applyseriesofopsca-operation"></a><span data-ttu-id="45be8-102">Bewerking ApplySeriesOfOpsCA</span><span class="sxs-lookup"><span data-stu-id="45be8-102">ApplySeriesOfOpsCA operation</span></span>

<span data-ttu-id="45be8-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="45be8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="45be8-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="45be8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="45be8-105">Past een lijst van OPS en hun doelen opeenvolgend toe op een matrix.</span><span class="sxs-lookup"><span data-stu-id="45be8-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="45be8-106">(Adjoint + beheerd)</span><span class="sxs-lookup"><span data-stu-id="45be8-106">(Adjoint + Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsCA<'T> (listOfOps : ('T[] => Unit is Adj + Ctl)[], targets : Int[][], register : 'T[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="45be8-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="45be8-107">Input</span></span>

### <a name="listofops--t--unit--is-adj--ctl"></a><span data-ttu-id="45be8-108">listOfOps: 'T [] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL []</span><span class="sxs-lookup"><span data-stu-id="45be8-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl[]</span></span>

<span data-ttu-id="45be8-109">De lijst met bewerkingen, waarbij elke matrix wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="45be8-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="45be8-110">Ze worden eerst opeenvolgend en laagste index toegepast.</span><span class="sxs-lookup"><span data-stu-id="45be8-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="45be8-111">Elk moet zowel een adjoint als een beheerde functor hebben.</span><span class="sxs-lookup"><span data-stu-id="45be8-111">Each must have both an Adjoint and Controlled functor.</span></span>


### <a name="targets--int"></a><span data-ttu-id="45be8-112">doelen: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="45be8-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="45be8-113">Geneste matrices waarin de doelen van de op-op worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="45be8-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="45be8-114">Elke matrix moet een lijst met ints bevatten waarin de indexen worden beschreven die moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="45be8-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="45be8-115">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="45be8-115">register : 'T[]</span></span>

<span data-ttu-id="45be8-116">Qubit-REGI ster waarop moet worden gehandeld.</span><span class="sxs-lookup"><span data-stu-id="45be8-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="45be8-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="45be8-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="45be8-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="45be8-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="45be8-119">T</span><span class="sxs-lookup"><span data-stu-id="45be8-119">'T</span></span>



## <a name="example"></a><span data-ttu-id="45be8-120">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="45be8-120">Example</span></span>

<span data-ttu-id="45be8-121">Het volgende is van toepassing exp ([PauliX, PauliY], 0,5) op qubits 0, 1//X tot Qubit 2 toestaan OPS = [exp ([PauliX, PauliY], 0,5, _), ApplyToFirstQubitCA (X, _)]; indices = [[0, 1], [2]]; ApplySeriesOfOpsCA (OPS, indices, qubitArray);</span><span class="sxs-lookup"><span data-stu-id="45be8-121">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubitCA(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOpsCA(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="45be8-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="45be8-122">See Also</span></span>

- [<span data-ttu-id="45be8-123">Micro soft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="45be8-123">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)