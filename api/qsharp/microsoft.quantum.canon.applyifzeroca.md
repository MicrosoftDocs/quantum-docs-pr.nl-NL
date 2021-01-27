---
uid: Microsoft.Quantum.Canon.ApplyIfZeroCA
title: Bewerking ApplyIfZeroCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroCA
qsharp.summary: Applies a unitary operation conditioned on a classical result value being zero.
ms.openlocfilehash: 4ed0660e2fe3623d0a8e4e4f3bd0bddb536b7b5c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98844882"
---
# <a name="applyifzeroca-operation"></a><span data-ttu-id="a846d-102">Bewerking ApplyIfZeroCA</span><span class="sxs-lookup"><span data-stu-id="a846d-102">ApplyIfZeroCA operation</span></span>

<span data-ttu-id="a846d-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a846d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a846d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a846d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a846d-105">Past een unitary-bewerking toe die is ingesteld op een klassieke resultaat waarde is nul.</span><span class="sxs-lookup"><span data-stu-id="a846d-105">Applies a unitary operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroCA<'T> (result : Result, (op : ('T => Unit is Adj + Ctl), target : 'T)) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="a846d-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a846d-106">Description</span></span>

<span data-ttu-id="a846d-107">`op` `result` `op` `target` Als dat zo is, geldt een bewerking en een resultaat waarde `result` `Zero` .</span><span class="sxs-lookup"><span data-stu-id="a846d-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="a846d-108">Als `One` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="a846d-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="a846d-109">Het achtervoegsel `CA` geeft aan dat de bewerking die moet worden toegepast, unitary is (adjointable).</span><span class="sxs-lookup"><span data-stu-id="a846d-109">The suffix `CA` indicates that the operation to be applied is unitary (controllable and adjointable).</span></span>

## <a name="input"></a><span data-ttu-id="a846d-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="a846d-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="a846d-111">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="a846d-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="a846d-112">Een meet resultaat dat bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="a846d-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="a846d-113">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="a846d-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="a846d-114">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="a846d-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="a846d-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="a846d-115">target : 'T</span></span>

<span data-ttu-id="a846d-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="a846d-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a846d-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a846d-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a846d-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a846d-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a846d-119">T</span><span class="sxs-lookup"><span data-stu-id="a846d-119">'T</span></span>

<span data-ttu-id="a846d-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="a846d-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="a846d-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a846d-121">See Also</span></span>

- [<span data-ttu-id="a846d-122">Micro soft. Quantum. Canon. ApplyIfZeroC</span><span class="sxs-lookup"><span data-stu-id="a846d-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="a846d-123">Micro soft. Quantum. Canon. ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="a846d-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="a846d-124">Micro soft. Quantum. Canon. ApplyIfZeroCA</span><span class="sxs-lookup"><span data-stu-id="a846d-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)