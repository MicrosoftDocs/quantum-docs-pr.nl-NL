---
uid: Microsoft.Quantum.Canon.ApplyIfElseR
title: Bewerking ApplyIfElseR
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyIfElseR
qsharp.summary: Applies one of two operations, depending on the value of a classical result.
ms.openlocfilehash: 0d7cc9f67f9dd0c69a9256f007a3aeab3e457907
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841802"
---
# <a name="applyifelser-operation"></a><span data-ttu-id="64405-102">Bewerking ApplyIfElseR</span><span class="sxs-lookup"><span data-stu-id="64405-102">ApplyIfElseR operation</span></span>

<span data-ttu-id="64405-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="64405-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="64405-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="64405-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="64405-105">Past een van de twee bewerkingen toe, afhankelijk van de waarde van een klassiek resultaat.</span><span class="sxs-lookup"><span data-stu-id="64405-105">Applies one of two operations, depending on the value of a classical result.</span></span>

```qsharp
operation ApplyIfElseR<'T, 'U> (result : Result, (zeroOp : ('T => Unit), zeroInput : 'T), (oneOp : ('U => Unit), oneInput : 'U)) : Unit
```


## <a name="description"></a><span data-ttu-id="64405-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="64405-106">Description</span></span>

<span data-ttu-id="64405-107">Als er een resultaat `result` is gegeven, wordt de bewerking `zeroOp` met `zeroInput` als invoer toegepast wanneer deze `result` gelijk is aan `Zero` en wordt toegepast `oneOp(oneInput)` Wanneer `result == One` .</span><span class="sxs-lookup"><span data-stu-id="64405-107">Given a result `result`, applies the operation `zeroOp` with `zeroInput` as its input when `result` is equal to `Zero`, and applies `oneOp(oneInput)` when `result == One`.</span></span>

## <a name="input"></a><span data-ttu-id="64405-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="64405-108">Input</span></span>

### <a name="result--__invalidresult__"></a><span data-ttu-id="64405-109">resultaat: __ongeldig <Result>__</span><span class="sxs-lookup"><span data-stu-id="64405-109">result : __invalid<Result>__</span></span>

<span data-ttu-id="64405-110">Het meet resultaat dat wordt gebruikt om te bepalen `zeroOp` of het `oneOp` wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="64405-110">The measurement result used to determine if `zeroOp` or `oneOp` is applied.</span></span>


### <a name="zeroop--t--unit"></a><span data-ttu-id="64405-111">zeroOp: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="64405-111">zeroOp : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="64405-112">De bewerking die moet worden toegepast wanneer `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="64405-112">The operation to be applied when `result == Zero`.</span></span>


### <a name="zeroinput--t"></a><span data-ttu-id="64405-113">zeroInput: 'T</span><span class="sxs-lookup"><span data-stu-id="64405-113">zeroInput : 'T</span></span>

<span data-ttu-id="64405-114">De invoer die moet worden opgegeven `zeroOp` als `result == Zero` .</span><span class="sxs-lookup"><span data-stu-id="64405-114">The input to be provided to `zeroOp` when `result == Zero`.</span></span>


### <a name="oneop--u--unit"></a><span data-ttu-id="64405-115">oneOp: ' U =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="64405-115">oneOp : 'U => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="64405-116">De bewerking die moet worden toegepast wanneer `result == One` .</span><span class="sxs-lookup"><span data-stu-id="64405-116">The operation to be applied when `result == One`.</span></span>


### <a name="oneinput--u"></a><span data-ttu-id="64405-117">oneInput: ' U</span><span class="sxs-lookup"><span data-stu-id="64405-117">oneInput : 'U</span></span>

<span data-ttu-id="64405-118">De invoer die moet worden opgegeven `oneOp` als `result == One` .</span><span class="sxs-lookup"><span data-stu-id="64405-118">The input to be provided to `oneOp` when `result == One`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="64405-119">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="64405-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="64405-120">Type parameters</span><span class="sxs-lookup"><span data-stu-id="64405-120">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="64405-121">T</span><span class="sxs-lookup"><span data-stu-id="64405-121">'T</span></span>

<span data-ttu-id="64405-122">Het invoer type van de bewerking `zeroOp` die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="64405-122">The input type of the operation `zeroOp` to be conditionally applied.</span></span>
### <a name="u"></a><span data-ttu-id="64405-123">' U</span><span class="sxs-lookup"><span data-stu-id="64405-123">'U</span></span>

<span data-ttu-id="64405-124">Het invoer type van de bewerking `oneOp` die voorwaardelijk moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="64405-124">The input type of the operation `oneOp` to be conditionally applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="64405-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="64405-125">See Also</span></span>

- [<span data-ttu-id="64405-126">Micro soft. Quantum. Canon. ApplyIfZero</span><span class="sxs-lookup"><span data-stu-id="64405-126">Microsoft.Quantum.Canon.ApplyIfZero</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfZero)
- [<span data-ttu-id="64405-127">Micro soft. Quantum. Canon. ApplyIfOne</span><span class="sxs-lookup"><span data-stu-id="64405-127">Microsoft.Quantum.Canon.ApplyIfOne</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfOne)
- [<span data-ttu-id="64405-128">Micro soft. Quantum. Canon. ApplyIfElseRC</span><span class="sxs-lookup"><span data-stu-id="64405-128">Microsoft.Quantum.Canon.ApplyIfElseRC</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRC)
- [<span data-ttu-id="64405-129">Micro soft. Quantum. Canon. ApplyIfElseRA</span><span class="sxs-lookup"><span data-stu-id="64405-129">Microsoft.Quantum.Canon.ApplyIfElseRA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRA)
- [<span data-ttu-id="64405-130">Micro soft. Quantum. Canon. ApplyIfElseRCA</span><span class="sxs-lookup"><span data-stu-id="64405-130">Microsoft.Quantum.Canon.ApplyIfElseRCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyIfElseRCA)