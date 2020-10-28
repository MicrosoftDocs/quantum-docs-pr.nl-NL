---
uid: Microsoft.Quantum.Canon.ApplyIfZeroC
title: Bewerking ApplyIfZeroC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroC
qsharp.summary: Applies a controllable operation conditioned on a classical result value being zero.
ms.openlocfilehash: cfc2a659f4da011baadff1a0d6a20a2a36d0a285
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705221"
---
# <a name="applyifzeroc-operation"></a><span data-ttu-id="a27fb-102">Bewerking ApplyIfZeroC</span><span class="sxs-lookup"><span data-stu-id="a27fb-102">ApplyIfZeroC operation</span></span>

<span data-ttu-id="a27fb-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a27fb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a27fb-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a27fb-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a27fb-105">Past een instelbaar bewerking toe die is voor bereid op een klassieke resultaat waarde is nul.</span><span class="sxs-lookup"><span data-stu-id="a27fb-105">Applies a controllable operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroC<'T> (result : Result, (op : ('T => Unit is Ctl), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="a27fb-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a27fb-106">Description</span></span>

<span data-ttu-id="a27fb-107">`op` `result` `op` `target` Als dat zo is, geldt een bewerking en een resultaat waarde `result` `Zero` .</span><span class="sxs-lookup"><span data-stu-id="a27fb-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="a27fb-108">Als `One` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="a27fb-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="a27fb-109">Het achtervoegsel `C` geeft aan dat de bewerking die moet worden toegepast, kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="a27fb-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="a27fb-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="a27fb-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="a27fb-111">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="a27fb-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="a27fb-112">Een meet resultaat dat bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="a27fb-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit-ctl"></a><span data-ttu-id="a27fb-113">op: 'T => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a27fb-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="a27fb-114">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="a27fb-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="a27fb-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="a27fb-115">target : 'T</span></span>

<span data-ttu-id="a27fb-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="a27fb-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a27fb-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a27fb-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a27fb-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a27fb-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a27fb-119">T</span><span class="sxs-lookup"><span data-stu-id="a27fb-119">'T</span></span>

<span data-ttu-id="a27fb-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="a27fb-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="a27fb-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a27fb-121">See Also</span></span>

- [<span data-ttu-id="a27fb-122">Micro soft. Quantum. Canon. ApplyIfZeroC</span><span class="sxs-lookup"><span data-stu-id="a27fb-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="a27fb-123">Micro soft. Quantum. Canon. ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="a27fb-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="a27fb-124">Micro soft. Quantum. Canon. ApplyIfZeroCA</span><span class="sxs-lookup"><span data-stu-id="a27fb-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)