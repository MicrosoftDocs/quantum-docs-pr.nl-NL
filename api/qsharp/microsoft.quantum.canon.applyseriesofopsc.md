---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsC
title: Bewerking ApplySeriesOfOpsC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsC
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Controlled)
ms.openlocfilehash: d909aadbfe86f6d1314e9be5434249c40932ae4a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705013"
---
# <a name="applyseriesofopsc-operation"></a><span data-ttu-id="d914b-102">Bewerking ApplySeriesOfOpsC</span><span class="sxs-lookup"><span data-stu-id="d914b-102">ApplySeriesOfOpsC operation</span></span>

<span data-ttu-id="d914b-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d914b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d914b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d914b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d914b-105">Past een lijst van OPS en hun doelen opeenvolgend toe op een matrix.</span><span class="sxs-lookup"><span data-stu-id="d914b-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="d914b-106">Gelijkrichter</span><span class="sxs-lookup"><span data-stu-id="d914b-106">(Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsC<'T> (listOfOps : ('T[] => Unit is Ctl)[], targets : Int[][], register : 'T[]) : Unit
```


## <a name="input"></a><span data-ttu-id="d914b-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="d914b-107">Input</span></span>

### <a name="listofops--t--unit-ctl"></a><span data-ttu-id="d914b-108">listOfOps: ' [] = CTL van>- [eenheid](xref:microsoft.quantum.lang-ref.unit) []</span><span class="sxs-lookup"><span data-stu-id="d914b-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl[]</span></span>

<span data-ttu-id="d914b-109">De lijst met bewerkingen, waarbij elke matrix wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="d914b-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="d914b-110">Ze worden eerst opeenvolgend en laagste index toegepast.</span><span class="sxs-lookup"><span data-stu-id="d914b-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="d914b-111">Elk moet een beheerde functor hebben</span><span class="sxs-lookup"><span data-stu-id="d914b-111">Each must have a Controlled functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="d914b-112">doelen: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="d914b-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="d914b-113">Geneste matrices waarin de doelen van de op-op worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="d914b-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="d914b-114">Elke matrix moet een lijst met ints bevatten waarin de indexen worden beschreven die moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d914b-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="d914b-115">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="d914b-115">register : 'T[]</span></span>

<span data-ttu-id="d914b-116">Qubit-REGI ster waarop moet worden gehandeld.</span><span class="sxs-lookup"><span data-stu-id="d914b-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d914b-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d914b-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d914b-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d914b-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d914b-119">T</span><span class="sxs-lookup"><span data-stu-id="d914b-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="d914b-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d914b-120">See Also</span></span>

- [<span data-ttu-id="d914b-121">Micro soft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="d914b-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)