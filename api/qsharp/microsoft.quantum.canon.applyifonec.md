---
uid: Microsoft.Quantum.Canon.ApplyIfOneC
title: Bewerking ApplyIfOneC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneC
qsharp.summary: Applies a controllable operation conditioned on a classical result value being one.
ms.openlocfilehash: 24a00d83c1bbe6b07adb27c58fc70bc76af0a910
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209414"
---
# <a name="applyifonec-operation"></a><span data-ttu-id="18764-102">Bewerking ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="18764-102">ApplyIfOneC operation</span></span>

<span data-ttu-id="18764-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="18764-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="18764-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="18764-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="18764-105">Hiermee wordt een instelbaar bewerking toegepast die is ingesteld op een klassieke resultaat waarde die één.</span><span class="sxs-lookup"><span data-stu-id="18764-105">Applies a controllable operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneC<'T> (result : Result, (op : ('T => Unit is Ctl), target : 'T)) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="18764-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="18764-106">Description</span></span>

<span data-ttu-id="18764-107">`op` `result` `op` `target` Als dat zo is, geldt een bewerking en een resultaat waarde `result` `One` .</span><span class="sxs-lookup"><span data-stu-id="18764-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="18764-108">Als `Zero` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="18764-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="18764-109">Het achtervoegsel `C` geeft aan dat de bewerking die moet worden toegepast, kan worden bestuurd.</span><span class="sxs-lookup"><span data-stu-id="18764-109">The suffix `C` indicates that the operation to be applied is controllable.</span></span>

## <a name="input"></a><span data-ttu-id="18764-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="18764-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="18764-111">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="18764-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="18764-112">Een meet resultaat dat bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="18764-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="18764-113">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="18764-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="18764-114">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="18764-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="18764-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="18764-115">target : 'T</span></span>

<span data-ttu-id="18764-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="18764-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="18764-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="18764-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="18764-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="18764-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="18764-119">T</span><span class="sxs-lookup"><span data-stu-id="18764-119">'T</span></span>

<span data-ttu-id="18764-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="18764-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="18764-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="18764-121">See Also</span></span>

- [<span data-ttu-id="18764-122">Micro soft. Quantum. Canon. ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="18764-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="18764-123">Micro soft. Quantum. Canon. ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="18764-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="18764-124">Micro soft. Quantum. Canon. ApplyIfOneCA</span><span class="sxs-lookup"><span data-stu-id="18764-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)