---
uid: Microsoft.Quantum.Canon.DelayCA
title: Bewerking DelayCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayCA
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: 4b4be55436d6619511a12c6fb7fbd0f23989152a
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704228"
---
# <a name="delayca-operation"></a><span data-ttu-id="d4184-102">Bewerking DelayCA</span><span class="sxs-lookup"><span data-stu-id="d4184-102">DelayCA operation</span></span>

<span data-ttu-id="d4184-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d4184-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d4184-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d4184-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d4184-105">Hiermee wordt een bepaalde bewerking toegepast met een vertraging.</span><span class="sxs-lookup"><span data-stu-id="d4184-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayCA<'T> (op : ('T => Unit is Ctl + Adj), arg : 'T, aux : Unit) : Unit
```


## <a name="description"></a><span data-ttu-id="d4184-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d4184-106">Description</span></span>

<span data-ttu-id="d4184-107">Op basis van een bewerking en een invoer voor die bewerking, wordt de bewerking toegepast wanneer er extra invoer is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="d4184-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="d4184-108">Met name de expressie `Delay(op, arg, _)` is een bewerking die van toepassing is `op` op `arg` Wanneer aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="d4184-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="d4184-109">Met expressie `Delay(op,arg,_)` kan de toepassing van worden uitgesteld `op` .</span><span class="sxs-lookup"><span data-stu-id="d4184-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="d4184-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="d4184-110">Input</span></span>

### <a name="op--t--unit-ctl--adj"></a><span data-ttu-id="d4184-111">op: 'T => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit) + correctie</span><span class="sxs-lookup"><span data-stu-id="d4184-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl + Adj</span></span>

<span data-ttu-id="d4184-112">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="d4184-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="d4184-113">arg: 'T</span><span class="sxs-lookup"><span data-stu-id="d4184-113">arg : 'T</span></span>

<span data-ttu-id="d4184-114">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="d4184-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="d4184-115">AUX: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d4184-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="d4184-116">Argument dat wordt gebruikt om de toepassing van de bewerking uit te stellen met behulp van een gedeeltelijke toepassing.</span><span class="sxs-lookup"><span data-stu-id="d4184-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d4184-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d4184-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d4184-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d4184-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d4184-119">T</span><span class="sxs-lookup"><span data-stu-id="d4184-119">'T</span></span>

<span data-ttu-id="d4184-120">Het invoer type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="d4184-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="d4184-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d4184-121">See Also</span></span>

- [<span data-ttu-id="d4184-122">Micro soft. Quantum. Canon. delay</span><span class="sxs-lookup"><span data-stu-id="d4184-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="d4184-123">Micro soft. Quantum. Canon. delayed</span><span class="sxs-lookup"><span data-stu-id="d4184-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)