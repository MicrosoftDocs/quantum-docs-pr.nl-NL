---
uid: Microsoft.Quantum.Canon.ApplyIfElseBC
title: Bewerking ApplyIfElseBC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseBC
qsharp.summary: Applies one of two controllable operations, depending on the value of a classical bit.
ms.openlocfilehash: ea06b0a0a07659407e13caa2baa4f3e37ca2a0f7
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96209516"
---
# <a name="applyifelsebc-operation"></a><span data-ttu-id="9e4c7-102">Bewerking ApplyIfElseBC</span><span class="sxs-lookup"><span data-stu-id="9e4c7-102">ApplyIfElseBC operation</span></span>

<span data-ttu-id="9e4c7-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9e4c7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9e4c7-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9e4c7-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9e4c7-105">Past een van de twee instel bare bewerkingen toe, afhankelijk van de waarde van een klassieke bit.</span><span class="sxs-lookup"><span data-stu-id="9e4c7-105">Applies one of two controllable operations, depending on the value of a classical bit.</span></span>

```qsharp
operation ApplyIfElseBC<'T, 'U> (bit : Bool, (trueOp : ('T => Unit is Ctl), trueInput : 'T), (falseOp : ('U => Unit is Ctl), falseInput : 'U)) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="9e4c7-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="9e4c7-106">Description</span></span>

<span data-ttu-id="9e4c7-107">Gezien een bit `bit` , wordt de bewerking `trueOp` met `trueInput` als invoer toegepast `bit` `true` en toegepast als dat zo `falseOp(falseInput)` is `bit` `false` .</span><span class="sxs-lookup"><span data-stu-id="9e4c7-107">Given a bit `bit`, applies the operation `trueOp` with `trueInput` as its input when `bit` is `true`, and applies `falseOp(falseInput)` when `bit` is `false`.</span></span>

## <a name="input"></a><span data-ttu-id="9e4c7-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="9e4c7-108">Input</span></span>

### <a name="bit--bool"></a><span data-ttu-id="9e4c7-109">bit: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9e4c7-109">bit : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>

<span data-ttu-id="9e4c7-110">De Booleaanse waarde die wordt gebruikt om te bepalen of deze `trueOp` `falseOp` is toegepast.</span><span class="sxs-lookup"><span data-stu-id="9e4c7-110">The boolean value used to determine whether `trueOp` or `falseOp` is applied.</span></span>


### <a name="trueop--t--unit--is-ctl"></a><span data-ttu-id="9e4c7-111">trueOp: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="9e4c7-111">trueOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="9e4c7-112">De instelbaar bewerking die moet worden toegepast wanneer dat het geval `bit` is `true` .</span><span class="sxs-lookup"><span data-stu-id="9e4c7-112">The controllable operation to be applied when `bit` is `true`.</span></span>


### <a name="trueinput--t"></a><span data-ttu-id="9e4c7-113">trueInput: 'T</span><span class="sxs-lookup"><span data-stu-id="9e4c7-113">trueInput : 'T</span></span>

<span data-ttu-id="9e4c7-114">De invoer die moet worden opgegeven `trueOp` als `bit` `true` .</span><span class="sxs-lookup"><span data-stu-id="9e4c7-114">The input to be provided to `trueOp` when `bit` is `true`.</span></span>


### <a name="falseop--u--unit--is-ctl"></a><span data-ttu-id="9e4c7-115">falseOp: ' U => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="9e4c7-115">falseOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="9e4c7-116">De instelbaar bewerking die moet worden toegepast wanneer dat het geval `bit` is `false` .</span><span class="sxs-lookup"><span data-stu-id="9e4c7-116">The controllable operation to be applied when `bit` is `false`.</span></span>


### <a name="falseinput--u"></a><span data-ttu-id="9e4c7-117">falseInput: ' U</span><span class="sxs-lookup"><span data-stu-id="9e4c7-117">falseInput : 'U</span></span>

<span data-ttu-id="9e4c7-118">De invoer die moet worden opgegeven `falseOp` als `bit` `false` .</span><span class="sxs-lookup"><span data-stu-id="9e4c7-118">The input to be provided to `falseOp` when `bit` is `false`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9e4c7-119">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9e4c7-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9e4c7-120">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9e4c7-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="9e4c7-121">T</span><span class="sxs-lookup"><span data-stu-id="9e4c7-121">'T</span></span>

<span data-ttu-id="9e4c7-122">Het invoer type van de bewerking `trueOp` die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="9e4c7-122">The input type of the operation `trueOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="9e4c7-123">' U</span><span class="sxs-lookup"><span data-stu-id="9e4c7-123">'U</span></span>

<span data-ttu-id="9e4c7-124">Het invoer type van de bewerking `falseOp` die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="9e4c7-124">The input type of the operation `falseOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="9e4c7-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9e4c7-125">See Also</span></span>

- [<span data-ttu-id="9e4c7-126">Micro soft. Quantum. Canon. ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="9e4c7-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="9e4c7-127">Micro soft. Quantum. Canon. ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="9e4c7-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="9e4c7-128">Micro soft. Quantum. Canon. ApplyIfElseRC</span><span class="sxs-lookup"><span data-stu-id="9e4c7-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="9e4c7-129">Micro soft. Quantum. Canon. ApplyIfElseRA</span><span class="sxs-lookup"><span data-stu-id="9e4c7-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="9e4c7-130">Micro soft. Quantum. Canon. ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="9e4c7-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)