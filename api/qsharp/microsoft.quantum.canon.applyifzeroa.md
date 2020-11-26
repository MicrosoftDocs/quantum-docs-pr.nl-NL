---
uid: Microsoft.Quantum.Canon.ApplyIfZeroA
title: Bewerking ApplyIfZeroA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being zero.
ms.openlocfilehash: ab5b05791213da7c8bee5915764c342cb0bed851
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218492"
---
# <a name="applyifzeroa-operation"></a><span data-ttu-id="d8ebb-102">Bewerking ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="d8ebb-102">ApplyIfZeroA operation</span></span>

<span data-ttu-id="d8ebb-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d8ebb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d8ebb-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="d8ebb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="d8ebb-105">Past een adjointable-bewerking toe die is ingesteld op een klassieke resultaat waarde is nul.</span><span class="sxs-lookup"><span data-stu-id="d8ebb-105">Applies an adjointable operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="d8ebb-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d8ebb-106">Description</span></span>

<span data-ttu-id="d8ebb-107">`op` `result` `op` `target` Als dat zo is, geldt een bewerking en een resultaat waarde `result` `Zero` .</span><span class="sxs-lookup"><span data-stu-id="d8ebb-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="d8ebb-108">Als `One` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="d8ebb-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="d8ebb-109">Het achtervoegsel `A` geeft aan dat de bewerking die moet worden toegepast, adjointable is.</span><span class="sxs-lookup"><span data-stu-id="d8ebb-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="d8ebb-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="d8ebb-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="d8ebb-111">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="d8ebb-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="d8ebb-112">Een meet resultaat dat bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="d8ebb-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-adj"></a><span data-ttu-id="d8ebb-113">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="d8ebb-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="d8ebb-114">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="d8ebb-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="d8ebb-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="d8ebb-115">target : 'T</span></span>

<span data-ttu-id="d8ebb-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="d8ebb-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d8ebb-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d8ebb-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d8ebb-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d8ebb-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d8ebb-119">T</span><span class="sxs-lookup"><span data-stu-id="d8ebb-119">'T</span></span>

<span data-ttu-id="d8ebb-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="d8ebb-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8ebb-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d8ebb-121">See Also</span></span>

- [<span data-ttu-id="d8ebb-122">Micro soft. Quantum. Canon. ApplyIfZeroC</span><span class="sxs-lookup"><span data-stu-id="d8ebb-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="d8ebb-123">Micro soft. Quantum. Canon. ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="d8ebb-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="d8ebb-124">Micro soft. Quantum. Canon. ApplyIfZeroCA</span><span class="sxs-lookup"><span data-stu-id="d8ebb-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)