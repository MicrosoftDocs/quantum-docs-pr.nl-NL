---
uid: Microsoft.Quantum.Canon.ApplyIfElseRCA
title: Bewerking ApplyIfElseRCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseRCA
qsharp.summary: Applies one of two unitary operations, depending on the value of a classical result.
ms.openlocfilehash: dfd1c16a25a2da507024813a380386c8f4e49d30
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96218747"
---
# <a name="applyifelserca-operation"></a><span data-ttu-id="dd999-102">Bewerking ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="dd999-102">ApplyIfElseRCA operation</span></span>

<span data-ttu-id="dd999-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="dd999-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="dd999-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="dd999-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="dd999-105">Past een van de twee unitary-bewerkingen toe, afhankelijk van de waarde van een klassiek resultaat.</span><span class="sxs-lookup"><span data-stu-id="dd999-105">Applies one of two unitary operations, depending on the value of a classical result.</span></span>

```qsharp
operation ApplyIfElseRCA<'T, 'U> (result : Result, (zeroOp : ('T => Unit is Adj + Ctl), zeroInput : 'T), (oneOp : ('U => Unit is Adj + Ctl), oneInput : 'U)) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="dd999-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="dd999-106">Description</span></span>

<span data-ttu-id="dd999-107">Als er een resultaat `result` is gegeven, wordt de bewerking `zeroOp` met `zeroInput` als invoer toegepast wanneer deze `result` gelijk is aan `Zero` en wordt toegepast `oneOp(oneInput)` Wanneer `result == One` .</span><span class="sxs-lookup"><span data-stu-id="dd999-107">Given a result `result`, applies the operation `zeroOp` with `zeroInput` as its input when `result` is equal to `Zero`, and applies `oneOp(oneInput)` when `result == One`.</span></span>

## <a name="input"></a><span data-ttu-id="dd999-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="dd999-108">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="dd999-109">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="dd999-109">result : __invalid<Result>__</span></span>

<span data-ttu-id="dd999-110">Het meet resultaat dat wordt gebruikt om te bepalen `zeroOp` of het `oneOp` wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="dd999-110">The measurement result used to determine if `zeroOp` or `oneOp` is applied.</span></span>


### <a name="zeroop--t--unit--is-adj--ctl"></a><span data-ttu-id="dd999-111">zeroOp: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="dd999-111">zeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="dd999-112">De unitary-bewerking die moet worden toegepast wanneer `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="dd999-112">The unitary operation to be applied when `result == Zero`.</span></span>


### <a name="zeroinput--t"></a><span data-ttu-id="dd999-113">zeroInput: 'T</span><span class="sxs-lookup"><span data-stu-id="dd999-113">zeroInput : 'T</span></span>

<span data-ttu-id="dd999-114">De invoer die moet worden opgegeven `zeroOp` als `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="dd999-114">The input to be provided to `zeroOp` when `result == Zero`.</span></span>


### <a name="oneop--u--unit--is-adj--ctl"></a><span data-ttu-id="dd999-115">oneOp: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="dd999-115">oneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="dd999-116">De unitary-bewerking die moet worden toegepast wanneer `result == One` .</span><span class="sxs-lookup"><span data-stu-id="dd999-116">The unitary operation to be applied when `result == One`.</span></span>


### <a name="oneinput--u"></a><span data-ttu-id="dd999-117">oneInput: ' U</span><span class="sxs-lookup"><span data-stu-id="dd999-117">oneInput : 'U</span></span>

<span data-ttu-id="dd999-118">De invoer die moet worden opgegeven `oneOp` als `result == One` .</span><span class="sxs-lookup"><span data-stu-id="dd999-118">The input to be provided to `oneOp` when `result == One`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="dd999-119">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="dd999-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="dd999-120">Type parameters</span><span class="sxs-lookup"><span data-stu-id="dd999-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="dd999-121">T</span><span class="sxs-lookup"><span data-stu-id="dd999-121">'T</span></span>

<span data-ttu-id="dd999-122">Het invoer type van de bewerking `zeroOp` die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="dd999-122">The input type of the operation `zeroOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="dd999-123">' U</span><span class="sxs-lookup"><span data-stu-id="dd999-123">'U</span></span>

<span data-ttu-id="dd999-124">Het invoer type van de bewerking `oneOp` die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="dd999-124">The input type of the operation `oneOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="dd999-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="dd999-125">See Also</span></span>

- [<span data-ttu-id="dd999-126">Micro soft. Quantum. Canon. ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="dd999-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="dd999-127">Micro soft. Quantum. Canon. ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="dd999-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="dd999-128">Micro soft. Quantum. Canon. ApplyIfElseRC</span><span class="sxs-lookup"><span data-stu-id="dd999-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="dd999-129">Micro soft. Quantum. Canon. ApplyIfElseRA</span><span class="sxs-lookup"><span data-stu-id="dd999-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="dd999-130">Micro soft. Quantum. Canon. ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="dd999-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)