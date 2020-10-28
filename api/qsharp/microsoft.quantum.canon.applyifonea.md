---
uid: Microsoft.Quantum.Canon.ApplyIfOneA
title: Bewerking ApplyIfOneA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfOneA
qsharp.summary: Applies an adjointable operation conditioned on a classical result value being one.
ms.openlocfilehash: 76c15aba6042c2801ecfe8470e82099c54ba3846
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705269"
---
# <a name="applyifonea-operation"></a><span data-ttu-id="6acf6-102">Bewerking ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="6acf6-102">ApplyIfOneA operation</span></span>

<span data-ttu-id="6acf6-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6acf6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6acf6-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="6acf6-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="6acf6-105">Hiermee wordt een adjointable-bewerking toegepast op een klassieke resultaat waarde die één.</span><span class="sxs-lookup"><span data-stu-id="6acf6-105">Applies an adjointable operation conditioned on a classical result value being one.</span></span>

```qsharp
operation ApplyIfOneA<'T> (result : Result, (op : ('T => Unit is Adj), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="6acf6-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6acf6-106">Description</span></span>

<span data-ttu-id="6acf6-107">`op` `result` `op` `target` Als dat zo is, geldt een bewerking en een resultaat waarde `result` `One` .</span><span class="sxs-lookup"><span data-stu-id="6acf6-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `One`.</span></span> <span data-ttu-id="6acf6-108">Als `Zero` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="6acf6-108">If `Zero`, nothing happens to the `target`.</span></span>
<span data-ttu-id="6acf6-109">Het achtervoegsel `A` geeft aan dat de bewerking die moet worden toegepast, adjointable is.</span><span class="sxs-lookup"><span data-stu-id="6acf6-109">The suffix `A` indicates that the operation to be applied is adjointable.</span></span>

## <a name="input"></a><span data-ttu-id="6acf6-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="6acf6-110">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="6acf6-111">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="6acf6-111">result : __invalid<Result>__</span></span>

<span data-ttu-id="6acf6-112">Een meet resultaat dat bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="6acf6-112">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit-adj"></a><span data-ttu-id="6acf6-113">op: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="6acf6-113">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="6acf6-114">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="6acf6-114">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="6acf6-115">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="6acf6-115">target : 'T</span></span>

<span data-ttu-id="6acf6-116">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="6acf6-116">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6acf6-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6acf6-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6acf6-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="6acf6-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6acf6-119">T</span><span class="sxs-lookup"><span data-stu-id="6acf6-119">'T</span></span>

<span data-ttu-id="6acf6-120">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="6acf6-120">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="6acf6-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6acf6-121">See Also</span></span>

- [<span data-ttu-id="6acf6-122">Micro soft. Quantum. Canon. ApplyIfOneC</span><span class="sxs-lookup"><span data-stu-id="6acf6-122">Microsoft.Quantum.Canon.ApplyIfOneC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneC)
- [<span data-ttu-id="6acf6-123">Micro soft. Quantum. Canon. ApplyIfOneA</span><span class="sxs-lookup"><span data-stu-id="6acf6-123">Microsoft.Quantum.Canon.ApplyIfOneA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneA)
- [<span data-ttu-id="6acf6-124">Micro soft. Quantum. Canon. ApplyIfOneCA</span><span class="sxs-lookup"><span data-stu-id="6acf6-124">Microsoft.Quantum.Canon.ApplyIfOneCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOneCA)