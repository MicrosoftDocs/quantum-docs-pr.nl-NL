---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsCA
title: Bewerking ApplySeriesOfOpsCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsCA
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Adjoint + Controlled)
ms.openlocfilehash: 2327a693e528cf46f95eae5ee052e9dd9b6ee187
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705005"
---
# <a name="applyseriesofopsca-operation"></a><span data-ttu-id="37d09-102">Bewerking ApplySeriesOfOpsCA</span><span class="sxs-lookup"><span data-stu-id="37d09-102">ApplySeriesOfOpsCA operation</span></span>

<span data-ttu-id="37d09-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="37d09-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="37d09-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="37d09-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="37d09-105">Past een lijst van OPS en hun doelen opeenvolgend toe op een matrix.</span><span class="sxs-lookup"><span data-stu-id="37d09-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="37d09-106">(Adjoint + beheerd)</span><span class="sxs-lookup"><span data-stu-id="37d09-106">(Adjoint + Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsCA<'T> (listOfOps : ('T[] => Unit is Adj + Ctl)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="37d09-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="37d09-107">Input</span></span>

### <a name="listofops--t--unit-adj--ctl"></a><span data-ttu-id="37d09-108">listOfOps: 'T [] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL []</span><span class="sxs-lookup"><span data-stu-id="37d09-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl[]</span></span>

<span data-ttu-id="37d09-109">De lijst met bewerkingen, waarbij elke matrix wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="37d09-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="37d09-110">Ze worden eerst opeenvolgend en laagste index toegepast.</span><span class="sxs-lookup"><span data-stu-id="37d09-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="37d09-111">Elk moet zowel een adjoint als een beheerde functor hebben.</span><span class="sxs-lookup"><span data-stu-id="37d09-111">Each must have both an Adjoint and Controlled functor.</span></span>


### <a name="targets--int"></a><span data-ttu-id="37d09-112">doelen: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="37d09-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="37d09-113">Geneste matrices waarin de doelen van de op-op worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="37d09-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="37d09-114">Elke matrix moet een lijst met ints bevatten waarin de indexen worden beschreven die moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="37d09-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="37d09-115">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="37d09-115">register : 'T[]</span></span>

<span data-ttu-id="37d09-116">Qubit-REGI ster waarop moet worden gehandeld.</span><span class="sxs-lookup"><span data-stu-id="37d09-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="37d09-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="37d09-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="37d09-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="37d09-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="37d09-119">T</span><span class="sxs-lookup"><span data-stu-id="37d09-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="37d09-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="37d09-120">See Also</span></span>

- [<span data-ttu-id="37d09-121">Micro soft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="37d09-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)