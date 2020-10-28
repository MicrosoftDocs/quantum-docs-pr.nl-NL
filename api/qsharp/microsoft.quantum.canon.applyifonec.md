---
uid: Microsoft.Quantum.Canon.ApplyIfOneC
title: Bewerking ApplyIfOneC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneC
qsharp.summary: Applies a controllable operation conditioned on a classical result value being one.
ms.openlocfilehash: 9a2e020c596b02d9cb38309d02ca02056c1dec75
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705268"
---
# <a name="applyifonec-operation"></a><span data-ttu-id="f0719-102">Bewerking ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="f0719-102">ApplyIfOneC operation</span></span>

<span data-ttu-id="f0719-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f0719-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f0719-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f0719-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f0719-105">Hiermee wordt een instelbaar bewerking toegepast die is ingesteld op een klassieke resultaat waarde die één.</span><span class="sxs-lookup"><span data-stu-id="f0719-105">Applies a controllable operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneC<'T> (result : Result, (op : ('T => Unit is Ctl), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="f0719-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f0719-106">Description</span></span>

<span data-ttu-id="f0719-107">`op` `result` `op` `target` Als dat zo is, geldt een bewerking en een resultaat waarde `result` `One` .</span><span class="sxs-lookup"><span data-stu-id="f0719-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="f0719-108">Als `Zero` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="f0719-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="f0719-109">Het achtervoegsel `C` geeft aan dat de bewerking die moet worden toegepast, kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="f0719-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="f0719-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="f0719-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="f0719-111">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="f0719-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="f0719-112">Een meet resultaat dat bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="f0719-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit-ctl"></a><span data-ttu-id="f0719-113">op: 'T => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f0719-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="f0719-114">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="f0719-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="f0719-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="f0719-115">target : 'T</span></span>

<span data-ttu-id="f0719-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="f0719-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f0719-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f0719-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f0719-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="f0719-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f0719-119">T</span><span class="sxs-lookup"><span data-stu-id="f0719-119">'T</span></span>

<span data-ttu-id="f0719-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="f0719-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0719-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f0719-121">See Also</span></span>

- [<span data-ttu-id="f0719-122">Micro soft. Quantum. Canon. ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="f0719-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="f0719-123">Micro soft. Quantum. Canon. ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="f0719-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="f0719-124">Micro soft. Quantum. Canon. ApplyIfOneCA</span><span class="sxs-lookup"><span data-stu-id="f0719-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)