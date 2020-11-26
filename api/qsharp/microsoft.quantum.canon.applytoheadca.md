---
uid: Microsoft.Quantum.Canon.ApplyToHeadCA
title: Bewerking ApplyToHeadCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadCA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: f28cff599e06090145fac860dbaf8274c966f80a
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208547"
---
# <a name="applytoheadca-operation"></a><span data-ttu-id="d831f-102">Bewerking ApplyToHeadCA</span><span class="sxs-lookup"><span data-stu-id="d831f-102">ApplyToHeadCA operation</span></span>

<span data-ttu-id="d831f-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d831f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d831f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d831f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d831f-105">Hiermee wordt een bewerking toegepast op het eerste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="d831f-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="d831f-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d831f-106">Description</span></span>

<span data-ttu-id="d831f-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="d831f-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="d831f-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="d831f-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="d831f-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="d831f-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="d831f-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="d831f-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="d831f-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="d831f-111">targets : 'T[]</span></span>

<span data-ttu-id="d831f-112">Een matrix met doelen waarop de eerste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="d831f-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d831f-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d831f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d831f-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d831f-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d831f-115">T</span><span class="sxs-lookup"><span data-stu-id="d831f-115">'T</span></span>

<span data-ttu-id="d831f-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="d831f-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="d831f-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d831f-117">See Also</span></span>

- [<span data-ttu-id="d831f-118">Micro soft. Quantum. Canon. ApplyToHead</span><span class="sxs-lookup"><span data-stu-id="d831f-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="d831f-119">Micro soft. Quantum. Canon. ApplyToHeadA</span><span class="sxs-lookup"><span data-stu-id="d831f-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="d831f-120">Micro soft. Quantum. Canon. ApplyToHeadC</span><span class="sxs-lookup"><span data-stu-id="d831f-120">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)