---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsC
title: Bewerking ApplySeriesOfOpsC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsC
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Controlled)
ms.openlocfilehash: eaa0ea3e33cce708af5879cfbe875397fbb82a8a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217931"
---
# <a name="applyseriesofopsc-operation"></a><span data-ttu-id="32a5c-102">Bewerking ApplySeriesOfOpsC</span><span class="sxs-lookup"><span data-stu-id="32a5c-102">ApplySeriesOfOpsC operation</span></span>

<span data-ttu-id="32a5c-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="32a5c-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="32a5c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="32a5c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="32a5c-105">Past een lijst van OPS en hun doelen opeenvolgend toe op een matrix.</span><span class="sxs-lookup"><span data-stu-id="32a5c-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="32a5c-106">Gelijkrichter</span><span class="sxs-lookup"><span data-stu-id="32a5c-106">(Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsC<'T> (listOfOps : ('T[] => Unit is Ctl)[], targets : Int[][], register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="32a5c-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="32a5c-107">Input</span></span>

### <a name="listofops--t--unit--is-ctl"></a><span data-ttu-id="32a5c-108">listOfOps: 'T [] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL []</span><span class="sxs-lookup"><span data-stu-id="32a5c-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl[]</span></span>

<span data-ttu-id="32a5c-109">De lijst met bewerkingen, waarbij elke matrix wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="32a5c-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="32a5c-110">Ze worden eerst opeenvolgend en laagste index toegepast.</span><span class="sxs-lookup"><span data-stu-id="32a5c-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="32a5c-111">Elk moet een beheerde functor hebben</span><span class="sxs-lookup"><span data-stu-id="32a5c-111">Each must have a Controlled functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="32a5c-112">doelen: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="32a5c-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="32a5c-113">Geneste matrices waarin de doelen van de op-op worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="32a5c-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="32a5c-114">Elke matrix moet een lijst met ints bevatten waarin de indexen worden beschreven die moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="32a5c-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="32a5c-115">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="32a5c-115">register : 'T[]</span></span>

<span data-ttu-id="32a5c-116">Qubit-REGI ster waarop moet worden gehandeld.</span><span class="sxs-lookup"><span data-stu-id="32a5c-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="32a5c-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="32a5c-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="32a5c-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="32a5c-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="32a5c-119">T</span><span class="sxs-lookup"><span data-stu-id="32a5c-119">'T</span></span>



## <a name="see-also"></a><span data-ttu-id="32a5c-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="32a5c-120">See Also</span></span>

- [<span data-ttu-id="32a5c-121">Micro soft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="32a5c-121">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)