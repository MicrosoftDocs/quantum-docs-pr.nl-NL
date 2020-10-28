---
uid: Microsoft.Quantum.Canon.ApplyIfOne
title: Bewerking ApplyIfOne
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOne
qsharp.summary: Applies an operation conditioned on a classical result value being one.
ms.openlocfilehash: 8c668423d126f02736bcb541e73e210a761c5719
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705276"
---
# <a name="applyifone-operation"></a><span data-ttu-id="3e2bc-102">Bewerking ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="3e2bc-102">ApplyIfOne operation</span></span>

<span data-ttu-id="3e2bc-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="3e2bc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="3e2bc-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="3e2bc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="3e2bc-105">Hiermee wordt een bewerking toegepast die is ingesteld op een klassieke resultaat waarde die één.</span><span class="sxs-lookup"><span data-stu-id="3e2bc-105">Applies an operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOne<'T> (result : Result, (op : ('T => Unit), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="3e2bc-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="3e2bc-106">Description</span></span>

<span data-ttu-id="3e2bc-107">`op` `result` `op` `target` Als dat zo is, geldt een bewerking en een resultaat waarde `result` `One` .</span><span class="sxs-lookup"><span data-stu-id="3e2bc-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="3e2bc-108">Als `Zero` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="3e2bc-108">If `Zero`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="3e2bc-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="3e2bc-109">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="3e2bc-110">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="3e2bc-110">result : __invalid<Result>__</span></span>

<span data-ttu-id="3e2bc-111">Een meet resultaat dat bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="3e2bc-111">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="3e2bc-112">op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3e2bc-112">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="3e2bc-113">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="3e2bc-113">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="3e2bc-114">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="3e2bc-114">target : 'T</span></span>

<span data-ttu-id="3e2bc-115">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="3e2bc-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="3e2bc-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="3e2bc-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="3e2bc-117">Type parameters</span><span class="sxs-lookup"><span data-stu-id="3e2bc-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="3e2bc-118">T</span><span class="sxs-lookup"><span data-stu-id="3e2bc-118">'T</span></span>

<span data-ttu-id="3e2bc-119">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="3e2bc-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="3e2bc-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3e2bc-120">See Also</span></span>

- [<span data-ttu-id="3e2bc-121">Micro soft. Quantum. Canon. ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="3e2bc-121">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="3e2bc-122">Micro soft. Quantum. Canon. ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="3e2bc-122">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="3e2bc-123">Micro soft. Quantum. Canon. ApplyIfOneCA</span><span class="sxs-lookup"><span data-stu-id="3e2bc-123">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)