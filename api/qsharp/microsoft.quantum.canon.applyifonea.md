---
uid: Microsoft.Quantum.Canon.ApplyIfOneA
title: Bewerking ApplyIfOneA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being one.
ms.openlocfilehash: 1593f565e950a9410df0ae9de59e6d0e6a7b99b0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844936"
---
# <a name="applyifonea-operation"></a><span data-ttu-id="415a8-102">Bewerking ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="415a8-102">ApplyIfOneA operation</span></span>

<span data-ttu-id="415a8-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="415a8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="415a8-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="415a8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="415a8-105">Hiermee wordt een adjointable-bewerking toegepast op een klassieke resultaat waarde die één.</span><span class="sxs-lookup"><span data-stu-id="415a8-105">Applies an adjointable operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="415a8-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="415a8-106">Description</span></span>

<span data-ttu-id="415a8-107">`op` `result` `op` `target` Als dat zo is, geldt een bewerking en een resultaat waarde `result` `One` .</span><span class="sxs-lookup"><span data-stu-id="415a8-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="415a8-108">Als `Zero` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="415a8-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="415a8-109">Het achtervoegsel `A` geeft aan dat de bewerking die moet worden toegepast, adjointable is.</span><span class="sxs-lookup"><span data-stu-id="415a8-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="415a8-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="415a8-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="415a8-111">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="415a8-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="415a8-112">Een meet resultaat dat bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="415a8-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-adj"></a><span data-ttu-id="415a8-113">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="415a8-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="415a8-114">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="415a8-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="415a8-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="415a8-115">target : 'T</span></span>

<span data-ttu-id="415a8-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="415a8-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="415a8-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="415a8-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="415a8-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="415a8-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="415a8-119">T</span><span class="sxs-lookup"><span data-stu-id="415a8-119">'T</span></span>

<span data-ttu-id="415a8-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="415a8-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="415a8-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="415a8-121">See Also</span></span>

- [<span data-ttu-id="415a8-122">Micro soft. Quantum. Canon. ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="415a8-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="415a8-123">Micro soft. Quantum. Canon. ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="415a8-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="415a8-124">Micro soft. Quantum. Canon. ApplyIfOneCA</span><span class="sxs-lookup"><span data-stu-id="415a8-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)