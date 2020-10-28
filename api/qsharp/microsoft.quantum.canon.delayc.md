---
uid: Microsoft.Quantum.Canon.DelayC
title: Bewerking DelayC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayC
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: acb817c3322063353dc08c5d6f8c539391b3bf39
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704237"
---
# <a name="delayc-operation"></a><span data-ttu-id="1a1d4-102">Bewerking DelayC</span><span class="sxs-lookup"><span data-stu-id="1a1d4-102">DelayC operation</span></span>

<span data-ttu-id="1a1d4-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="1a1d4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="1a1d4-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="1a1d4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="1a1d4-105">Hiermee wordt een bepaalde bewerking toegepast met een vertraging.</span><span class="sxs-lookup"><span data-stu-id="1a1d4-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayC<'T> (op : ('T => Unit is Ctl), arg : 'T, aux : Unit) : Unit
```


## <a name="description"></a><span data-ttu-id="1a1d4-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="1a1d4-106">Description</span></span>

<span data-ttu-id="1a1d4-107">Op basis van een bewerking en een invoer voor die bewerking, wordt de bewerking toegepast wanneer er extra invoer is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="1a1d4-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="1a1d4-108">Met name de expressie `Delay(op, arg, _)` is een bewerking die van toepassing is `op` op `arg` Wanneer aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="1a1d4-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="1a1d4-109">Met expressie `Delay(op,arg,_)` kan de toepassing van worden uitgesteld `op` .</span><span class="sxs-lookup"><span data-stu-id="1a1d4-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="1a1d4-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="1a1d4-110">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="1a1d4-111">op: 'T => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1a1d4-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="1a1d4-112">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="1a1d4-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="1a1d4-113">arg: 'T</span><span class="sxs-lookup"><span data-stu-id="1a1d4-113">arg : 'T</span></span>

<span data-ttu-id="1a1d4-114">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="1a1d4-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="1a1d4-115">AUX: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1a1d4-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="1a1d4-116">Argument dat wordt gebruikt om de toepassing van de bewerking uit te stellen met behulp van een gedeeltelijke toepassing.</span><span class="sxs-lookup"><span data-stu-id="1a1d4-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="1a1d4-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="1a1d4-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="1a1d4-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="1a1d4-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="1a1d4-119">T</span><span class="sxs-lookup"><span data-stu-id="1a1d4-119">'T</span></span>

<span data-ttu-id="1a1d4-120">Het invoer type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="1a1d4-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="1a1d4-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1a1d4-121">See Also</span></span>

- [<span data-ttu-id="1a1d4-122">Micro soft. Quantum. Canon. delay</span><span class="sxs-lookup"><span data-stu-id="1a1d4-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="1a1d4-123">Micro soft. Quantum. Canon. delayed</span><span class="sxs-lookup"><span data-stu-id="1a1d4-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)