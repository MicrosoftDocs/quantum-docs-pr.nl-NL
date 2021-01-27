---
uid: Microsoft.Quantum.Canon.ApplySeriesOfOpsC
title: Bewerking ApplySeriesOfOpsC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplySeriesOfOpsC
qsharp.summary: Applies a list of ops and their targets sequentially on an array. (Controlled)
ms.openlocfilehash: 308256833dc607f685e3a5f2278e374cf3b6ce22
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844650"
---
# <a name="applyseriesofopsc-operation"></a><span data-ttu-id="2dcd3-102">Bewerking ApplySeriesOfOpsC</span><span class="sxs-lookup"><span data-stu-id="2dcd3-102">ApplySeriesOfOpsC operation</span></span>

<span data-ttu-id="2dcd3-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="2dcd3-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="2dcd3-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2dcd3-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2dcd3-105">Past een lijst van OPS en hun doelen opeenvolgend toe op een matrix.</span><span class="sxs-lookup"><span data-stu-id="2dcd3-105">Applies a list of ops and their targets sequentially on an array.</span></span> <span data-ttu-id="2dcd3-106">Gelijkrichter</span><span class="sxs-lookup"><span data-stu-id="2dcd3-106">(Controlled)</span></span>

```qsharp
operation ApplySeriesOfOpsC<'T> (listOfOps : ('T[] => Unit is Ctl)[], targets : Int[][], register : 'T[]) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="2dcd3-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="2dcd3-107">Input</span></span>

### <a name="listofops--t--unit--is-ctl"></a><span data-ttu-id="2dcd3-108">listOfOps: 'T [] =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL []</span><span class="sxs-lookup"><span data-stu-id="2dcd3-108">listOfOps : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl[]</span></span>

<span data-ttu-id="2dcd3-109">De lijst met bewerkingen, waarbij elke matrix wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="2dcd3-109">List of ops, each taking a 'T array, to be applied.</span></span> <span data-ttu-id="2dcd3-110">Ze worden eerst opeenvolgend en laagste index toegepast.</span><span class="sxs-lookup"><span data-stu-id="2dcd3-110">They are applied sequentially, lowest index first.</span></span>
<span data-ttu-id="2dcd3-111">Elk moet een beheerde functor hebben</span><span class="sxs-lookup"><span data-stu-id="2dcd3-111">Each must have a Controlled functor</span></span>


### <a name="targets--int"></a><span data-ttu-id="2dcd3-112">doelen: [int](xref:microsoft.quantum.lang-ref.int)[] []</span><span class="sxs-lookup"><span data-stu-id="2dcd3-112">targets : [Int](xref:microsoft.quantum.lang-ref.int)[][]</span></span>

<span data-ttu-id="2dcd3-113">Geneste matrices waarin de doelen van de op-op worden beschreven.</span><span class="sxs-lookup"><span data-stu-id="2dcd3-113">Nested arrays describing the targets of the op.</span></span> <span data-ttu-id="2dcd3-114">Elke matrix moet een lijst met ints bevatten waarin de indexen worden beschreven die moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="2dcd3-114">Each array should contain a list of ints describing the indices to be used.</span></span>


### <a name="register--t"></a><span data-ttu-id="2dcd3-115">registreren: 'T []</span><span class="sxs-lookup"><span data-stu-id="2dcd3-115">register : 'T[]</span></span>

<span data-ttu-id="2dcd3-116">Qubit-REGI ster waarop moet worden gehandeld.</span><span class="sxs-lookup"><span data-stu-id="2dcd3-116">Qubit register to be acted upon.</span></span>



## <a name="output--unit"></a><span data-ttu-id="2dcd3-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="2dcd3-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="2dcd3-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="2dcd3-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="2dcd3-119">T</span><span class="sxs-lookup"><span data-stu-id="2dcd3-119">'T</span></span>



## <a name="example"></a><span data-ttu-id="2dcd3-120">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="2dcd3-120">Example</span></span>

<span data-ttu-id="2dcd3-121">Het volgende is van toepassing exp ([PauliX, PauliY], 0,5) op qubits 0, 1//X tot Qubit 2 toestaan OPS = [exp ([PauliX, PauliY], 0,5, _), ApplyToFirstQubitC (X, _)]; indices = [[0, 1], [2]]; ApplySeriesOfOpsC (OPS, indices, qubitArray);</span><span class="sxs-lookup"><span data-stu-id="2dcd3-121">// The following applies Exp([PauliX, PauliY], 0.5) to qubits 0, 1 // then X to qubit 2 let ops = [Exp([PauliX, PauliY], 0.5, _), ApplyToFirstQubitC(X, _)]; let indices = [[0, 1], [2]]; ApplySeriesOfOpsC(ops, indices, qubitArray);</span></span>

## <a name="see-also"></a><span data-ttu-id="2dcd3-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2dcd3-122">See Also</span></span>

- [<span data-ttu-id="2dcd3-123">Micro soft. Quantum. Canon. ApplyOpRepeatedlyOver</span><span class="sxs-lookup"><span data-stu-id="2dcd3-123">Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver</span></span>](xref:Microsoft.Quantum.Canon.ApplyOpRepeatedlyOver)