---
uid: Microsoft.Quantum.Canon.ApplyToHeadC
title: Bewerking ApplyToHeadC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadC
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 3ff6c25837f1219dd456bf1739a2953ff72e2df9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704788"
---
# <a name="applytoheadc-operation"></a><span data-ttu-id="9f8b6-102">Bewerking ApplyToHeadC</span><span class="sxs-lookup"><span data-stu-id="9f8b6-102">ApplyToHeadC operation</span></span>

<span data-ttu-id="9f8b6-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9f8b6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9f8b6-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9f8b6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9f8b6-105">Hiermee wordt een bewerking toegepast op het eerste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="9f8b6-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="9f8b6-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="9f8b6-106">Description</span></span>

<span data-ttu-id="9f8b6-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="9f8b6-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="9f8b6-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="9f8b6-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="9f8b6-109">op: 'T => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9f8b6-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="9f8b6-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="9f8b6-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="9f8b6-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="9f8b6-111">targets : 'T[]</span></span>

<span data-ttu-id="9f8b6-112">Een matrix met doelen waarop de eerste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="9f8b6-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9f8b6-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9f8b6-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9f8b6-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9f8b6-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9f8b6-115">T</span><span class="sxs-lookup"><span data-stu-id="9f8b6-115">'T</span></span>

<span data-ttu-id="9f8b6-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="9f8b6-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="9f8b6-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9f8b6-117">See Also</span></span>

- [<span data-ttu-id="9f8b6-118">Micro soft. Quantum. Canon. ApplyToHead</span><span class="sxs-lookup"><span data-stu-id="9f8b6-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="9f8b6-119">Micro soft. Quantum. Canon. ApplyToHeadA</span><span class="sxs-lookup"><span data-stu-id="9f8b6-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="9f8b6-120">Micro soft. Quantum. Canon. ApplyToHeadCA</span><span class="sxs-lookup"><span data-stu-id="9f8b6-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)