---
uid: Microsoft.Quantum.Canon.ApplyIfZero
title: Bewerking ApplyIfZero
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfZero
qsharp.summary: Applies an operation conditioned on a classical result value being zero.
ms.openlocfilehash: 3b14ef8a1aa736fe096a21fe51be5a7c5bb1d09d
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209430"
---
# <a name="applyifzero-operation"></a><span data-ttu-id="59f16-102">Bewerking ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="59f16-102">ApplyIfZero operation</span></span>

<span data-ttu-id="59f16-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="59f16-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="59f16-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="59f16-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="59f16-105">Hiermee wordt een bewerking die is ingesteld op een klassieke resultaat waarde, ingesteld op nul.</span><span class="sxs-lookup"><span data-stu-id="59f16-105">Applies an operation conditioned on a classical result value being zero.</span></span>

```qsharp
operation ApplyIfZero<'T> (result : Result, (op : ('T => Unit), target : 'T)) : Unit
```


## <a name="description"></a><span data-ttu-id="59f16-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="59f16-106">Description</span></span>

<span data-ttu-id="59f16-107">`op` `result` `op` `target` Als dat zo is, geldt een bewerking en een resultaat waarde `result` `Zero` .</span><span class="sxs-lookup"><span data-stu-id="59f16-107">Given an operation `op` and a result value `result`, applies `op` to the `target` if `result` is `Zero`.</span></span> <span data-ttu-id="59f16-108">Als `One` , gebeurt er niets met `target` .</span><span class="sxs-lookup"><span data-stu-id="59f16-108">If `One`, nothing happens to the `target`.</span></span>

## <a name="input"></a><span data-ttu-id="59f16-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="59f16-109">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="59f16-110">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="59f16-110">result : __invalid<Result>__</span></span>

<span data-ttu-id="59f16-111">Een meet resultaat dat bepaalt of op wordt toegepast of niet.</span><span class="sxs-lookup"><span data-stu-id="59f16-111">A measurement result that controls whether op is applied or not.</span></span>


### <a name="op--t--unit"></a><span data-ttu-id="59f16-112">op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="59f16-112">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="59f16-113">Een bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="59f16-113">An operation to be conditionally applied.</span></span>


### <a name="target--t"></a><span data-ttu-id="59f16-114">doel: 'T</span><span class="sxs-lookup"><span data-stu-id="59f16-114">target : 'T</span></span>

<span data-ttu-id="59f16-115">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="59f16-115">The input to which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="59f16-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="59f16-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="59f16-117">Type parameters</span><span class="sxs-lookup"><span data-stu-id="59f16-117">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="59f16-118">T</span><span class="sxs-lookup"><span data-stu-id="59f16-118">'T</span></span>

<span data-ttu-id="59f16-119">Het invoer type van de bewerking die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="59f16-119">The input type of the operation to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="59f16-120">Zie ook</span><span class="sxs-lookup"><span data-stu-id="59f16-120">See Also</span></span>

- [<span data-ttu-id="59f16-121">Micro soft. Quantum. Canon. ApplyIfZeroC</span><span class="sxs-lookup"><span data-stu-id="59f16-121">Microsoft.Quantum.Canon.ApplyIfZeroC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroC)
- [<span data-ttu-id="59f16-122">Micro soft. Quantum. Canon. ApplyIfZeroA</span><span class="sxs-lookup"><span data-stu-id="59f16-122">Microsoft.Quantum.Canon.ApplyIfZeroA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroA)
- [<span data-ttu-id="59f16-123">Micro soft. Quantum. Canon. ApplyIfZeroCA</span><span class="sxs-lookup"><span data-stu-id="59f16-123">Microsoft.Quantum.Canon.ApplyIfZeroCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZeroCA)