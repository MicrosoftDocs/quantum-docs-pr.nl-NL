---
uid: Microsoft.Quantum.Canon.ApplyIfZeroA
title: Bewerking ApplyIfZeroA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZeroA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being zero.
ms.openlocfilehash: d324cd970e8df49ceb51b6bf5c9f3c9c3ff142f9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705245"
---
# <a name="applyifzeroa-operation"></a><span data-ttu-id="afbb5-102">Bewerking ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="afbb5-102">ApplyIfZeroA operation</span></span>

<span data-ttu-id="afbb5-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="afbb5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="afbb5-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="afbb5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="afbb5-105">Past een adjointable-bewerking toe die is ingesteld op een klassieke resultaat waarde is nul.</span><span class="sxs-lookup"><span data-stu-id="afbb5-105">Applies an adjointable operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZeroA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="afbb5-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="afbb5-106">Description</span></span>

<span data-ttu-id="afbb5-107">`op` `result` `op` `target` Als dat zo is, geldt een bewerking en een resultaat waarde `result` `Zero` .</span><span class="sxs-lookup"><span data-stu-id="afbb5-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="afbb5-108">Als `One` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="afbb5-108">If `One`, nothing happens to the `target`.</span></span>
<span data-ttu-id="afbb5-109">Het achtervoegsel `A` geeft aan dat de bewerking die moet worden toegepast, adjointable is.</span><span class="sxs-lookup"><span data-stu-id="afbb5-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="afbb5-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="afbb5-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="afbb5-111">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="afbb5-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="afbb5-112">Een meet resultaat dat bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="afbb5-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit-adj"></a><span data-ttu-id="afbb5-113">op: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="afbb5-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="afbb5-114">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="afbb5-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="afbb5-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="afbb5-115">target : 'T</span></span>

<span data-ttu-id="afbb5-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="afbb5-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="afbb5-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="afbb5-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="afbb5-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="afbb5-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="afbb5-119">T</span><span class="sxs-lookup"><span data-stu-id="afbb5-119">'T</span></span>

<span data-ttu-id="afbb5-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="afbb5-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="afbb5-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="afbb5-121">See Also</span></span>

- [<span data-ttu-id="afbb5-122">Micro soft. Quantum. Canon. ApplyIfZeroC</span><span class="sxs-lookup"><span data-stu-id="afbb5-122">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="afbb5-123">Micro soft. Quantum. Canon. ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="afbb5-123">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="afbb5-124">Micro soft. Quantum. Canon. ApplyIfZeroCA</span><span class="sxs-lookup"><span data-stu-id="afbb5-124">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)