---
uid: Microsoft.Quantum.Canon.ApplyToHeadCA
title: Bewerking ApplyToHeadCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHeadCA
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 1bb24006a2d52167dfc7a7871cfbf5a4378d1cb7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850615"
---
# <a name="applytoheadca-operation"></a><span data-ttu-id="cc74e-102">Bewerking ApplyToHeadCA</span><span class="sxs-lookup"><span data-stu-id="cc74e-102">ApplyToHeadCA operation</span></span>

<span data-ttu-id="cc74e-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="cc74e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="cc74e-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="cc74e-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="cc74e-105">Hiermee wordt een bewerking toegepast op het eerste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="cc74e-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHeadCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="cc74e-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="cc74e-106">Description</span></span>

<span data-ttu-id="cc74e-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="cc74e-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="cc74e-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="cc74e-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="cc74e-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="cc74e-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="cc74e-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="cc74e-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="cc74e-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="cc74e-111">targets : 'T[]</span></span>

<span data-ttu-id="cc74e-112">Een matrix met doelen waarop de eerste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="cc74e-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="cc74e-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="cc74e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="cc74e-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="cc74e-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="cc74e-115">T</span><span class="sxs-lookup"><span data-stu-id="cc74e-115">'T</span></span>

<span data-ttu-id="cc74e-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="cc74e-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="cc74e-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="cc74e-117">See Also</span></span>

- [<span data-ttu-id="cc74e-118">Micro soft. Quantum. Canon. ApplyToHead</span><span class="sxs-lookup"><span data-stu-id="cc74e-118">Microsoft.Quantum.Canon.ApplyToHead</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHead)
- [<span data-ttu-id="cc74e-119">Micro soft. Quantum. Canon. ApplyToHeadA</span><span class="sxs-lookup"><span data-stu-id="cc74e-119">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="cc74e-120">Micro soft. Quantum. Canon. ApplyToHeadC</span><span class="sxs-lookup"><span data-stu-id="cc74e-120">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)