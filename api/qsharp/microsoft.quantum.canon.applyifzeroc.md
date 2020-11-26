---
uid: Microsoft.Quantum.Canon.ApplyIfZeroC
title: Bewerking ApplyIfZeroC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroC
qsharp.summary: Applies a controllable operation conditioned on a classical result value being zero.
ms.openlocfilehash: c89490b13d946d119f3fd38d130d90847d67fea6
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209346"
---
# <a name="applyifzeroc-operation"></a><span data-ttu-id="5867a-102">Bewerking ApplyIfZeroC</span><span class="sxs-lookup"><span data-stu-id="5867a-102">ApplyIfZeroC operation</span></span>

<span data-ttu-id="5867a-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5867a-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5867a-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="5867a-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="5867a-105">Past een instelbaar bewerking toe die is voor bereid op een klassieke resultaat waarde is nul.</span><span class="sxs-lookup"><span data-stu-id="5867a-105">Applies a controllable operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroC<'T> (result : Result, (op : ('T => Unit is Ctl), target : 'T)) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="5867a-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="5867a-106">Description</span></span>

<span data-ttu-id="5867a-107">`op` `result` `op` `target` Als dat zo is, geldt een bewerking en een resultaat waarde `result` `Zero` .</span><span class="sxs-lookup"><span data-stu-id="5867a-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="5867a-108">Als `One` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="5867a-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="5867a-109">Het achtervoegsel `C` geeft aan dat de bewerking die moet worden toegepast, kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="5867a-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="5867a-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="5867a-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="5867a-111">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="5867a-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="5867a-112">Een meet resultaat dat bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="5867a-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="5867a-113">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="5867a-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="5867a-114">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="5867a-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="5867a-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="5867a-115">target : 'T</span></span>

<span data-ttu-id="5867a-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="5867a-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5867a-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5867a-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5867a-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="5867a-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5867a-119">T</span><span class="sxs-lookup"><span data-stu-id="5867a-119">'T</span></span>

<span data-ttu-id="5867a-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="5867a-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="5867a-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5867a-121">See Also</span></span>

- [<span data-ttu-id="5867a-122">Micro soft. Quantum. Canon. ApplyIfZeroC</span><span class="sxs-lookup"><span data-stu-id="5867a-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="5867a-123">Micro soft. Quantum. Canon. ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="5867a-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="5867a-124">Micro soft. Quantum. Canon. ApplyIfZeroCA</span><span class="sxs-lookup"><span data-stu-id="5867a-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)