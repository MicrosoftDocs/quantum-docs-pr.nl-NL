---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsA
title: Bewerking ApplySeriesOfOpsA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint)
ms.openlocfilehash: e5b3527507f79dcc77803ce01472856145df0e9f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217965"
---
# <a name="applyseriesofopsa-operation"></a><span data-ttu-id="be811-102">Bewerking ApplySeriesOfOpsA</span><span class="sxs-lookup"><span data-stu-id="be811-102">ApplySeriesOfOpsA operation</span></span>

<span data-ttu-id="be811-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="be811-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="be811-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="be811-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="be811-105">Past een lijst van OPS en hun doelen opeenvolgend toe op een matrix.</span><span class="sxs-lookup"><span data-stu-id="be811-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="be811-106">(Adjoint)</span><span class="sxs-lookup"><span data-stu-id="be811-106">(Adjoint)</span></span>

```qsharp
operation ApplySeriesOfOpsA<'T> (listOfOps : ('T[] => Unit is Adj)[], targets : Int[][], register : 'T[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="be811-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="be811-107">Input</span></span>

### <a name="listofops--t--unit--is-adj"></a><span data-ttu-id="be811-108">listOfOps: 'T [] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ []</span><span class="sxs-lookup"><span data-stu-id="be811-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj[]</span></span>

<span data-ttu-id="be811-109">De lijst met bewerkingen, waarbij elke matrix wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="be811-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="be811-110">Ze worden eerst opeenvolgend en laagste index toegepast.</span><span class="sxs-lookup"><span data-stu-id="be811-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="be811-111">Elk moet een adjoint-functor hebben</span><span class="sxs-lookup"><span data-stu-id="be811-111">Each must have an adjoint functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="be811-112">doelen: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="be811-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="be811-113">Geneste matrices waarin de doelen van de op-op worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="be811-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="be811-114">Elke matrix moet een lijst met ints bevatten waarin de indexen worden beschreven die moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="be811-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="be811-115">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="be811-115">register : 'T[]</span></span>

<span data-ttu-id="be811-116">Qubit-REGI ster waarop moet worden gehandeld.</span><span class="sxs-lookup"><span data-stu-id="be811-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="be811-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="be811-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="be811-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="be811-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="be811-119">T</span><span class="sxs-lookup"><span data-stu-id="be811-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="be811-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="be811-120">See Also</span></span>

- [<span data-ttu-id="be811-121">Micro soft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="be811-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)