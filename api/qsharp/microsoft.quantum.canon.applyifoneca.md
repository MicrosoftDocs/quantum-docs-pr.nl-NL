---
uid: Microsoft.Quantum.Canon.ApplyIfOneCA
title: Bewerking ApplyIfOneCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneCA
qsharp.summary: Applies a unitary operation conditioned on a classical result value being one.
ms.openlocfilehash: 973dd3c5f9f3e9ad03c0626a38779f499b7ce657
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705253"
---
# <a name="applyifoneca-operation"></a><span data-ttu-id="80bea-102">Bewerking ApplyIfOneCA</span><span class="sxs-lookup"><span data-stu-id="80bea-102">ApplyIfOneCA operation</span></span>

<span data-ttu-id="80bea-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="80bea-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="80bea-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="80bea-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="80bea-105">Hiermee wordt een unitary-bewerking toegepast op een klassieke resultaat waarde die één.</span><span class="sxs-lookup"><span data-stu-id="80bea-105">Applies a unitary operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneCA<'T> (result : Result, (op : ('T => Unit is Adj + Ctl), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="80bea-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="80bea-106">Description</span></span>

<span data-ttu-id="80bea-107">`op` `result` `op` `target` Als dat zo is, geldt een bewerking en een resultaat waarde `result` `One` .</span><span class="sxs-lookup"><span data-stu-id="80bea-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="80bea-108">Als `Zero` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="80bea-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="80bea-109">Het achtervoegsel `CA` geeft aan dat de bewerking die moet worden toegepast, unitary is (adjointable).</span><span class="sxs-lookup"><span data-stu-id="80bea-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="80bea-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="80bea-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="80bea-111">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="80bea-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="80bea-112">Een meet resultaat dat bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="80bea-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit-adj--ctl"></a><span data-ttu-id="80bea-113">op: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="80bea-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="80bea-114">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="80bea-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="80bea-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="80bea-115">target : 'T</span></span>

<span data-ttu-id="80bea-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="80bea-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="80bea-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="80bea-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="80bea-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="80bea-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="80bea-119">T</span><span class="sxs-lookup"><span data-stu-id="80bea-119">'T</span></span>

<span data-ttu-id="80bea-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="80bea-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="80bea-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="80bea-121">See Also</span></span>

- [<span data-ttu-id="80bea-122">Micro soft. Quantum. Canon. ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="80bea-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="80bea-123">Micro soft. Quantum. Canon. ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="80bea-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="80bea-124">Micro soft. Quantum. Canon. ApplyIfOneCA</span><span class="sxs-lookup"><span data-stu-id="80bea-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)