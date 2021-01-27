---
uid: Microsoft.Quantum.Canon.ApplyIfZeroC
title: Bewerking ApplyIfZeroC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroC
qsharp.summary: Applies a controllable operation conditioned on a classical result value being zero.
ms.openlocfilehash: 3876e2baf1b3ad5bbfa0097d468b1e88adf05db4
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841722"
---
# <a name="applyifzeroc-operation"></a><span data-ttu-id="e45fe-102">Bewerking ApplyIfZeroC</span><span class="sxs-lookup"><span data-stu-id="e45fe-102">ApplyIfZeroC operation</span></span>

<span data-ttu-id="e45fe-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e45fe-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e45fe-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e45fe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e45fe-105">Past een instelbaar bewerking toe die is voor bereid op een klassieke resultaat waarde is nul.</span><span class="sxs-lookup"><span data-stu-id="e45fe-105">Applies a controllable operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroC<'T> (result : Result, (op : ('T => Unit is Ctl), target : 'T)) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="e45fe-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e45fe-106">Description</span></span>

<span data-ttu-id="e45fe-107">`op` `result` `op` `target` Als dat zo is, geldt een bewerking en een resultaat waarde `result` `Zero` .</span><span class="sxs-lookup"><span data-stu-id="e45fe-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="e45fe-108">Als `One` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="e45fe-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="e45fe-109">Het achtervoegsel `C` geeft aan dat de bewerking die moet worden toegepast, kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="e45fe-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="e45fe-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="e45fe-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="e45fe-111">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="e45fe-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="e45fe-112">Een meet resultaat dat bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="e45fe-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="e45fe-113">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="e45fe-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="e45fe-114">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e45fe-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="e45fe-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="e45fe-115">target : 'T</span></span>

<span data-ttu-id="e45fe-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="e45fe-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e45fe-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e45fe-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e45fe-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e45fe-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e45fe-119">T</span><span class="sxs-lookup"><span data-stu-id="e45fe-119">'T</span></span>

<span data-ttu-id="e45fe-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e45fe-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="e45fe-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e45fe-121">See Also</span></span>

- [<span data-ttu-id="e45fe-122">Micro soft. Quantum. Canon. ApplyIfZeroC</span><span class="sxs-lookup"><span data-stu-id="e45fe-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="e45fe-123">Micro soft. Quantum. Canon. ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="e45fe-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="e45fe-124">Micro soft. Quantum. Canon. ApplyIfZeroCA</span><span class="sxs-lookup"><span data-stu-id="e45fe-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)