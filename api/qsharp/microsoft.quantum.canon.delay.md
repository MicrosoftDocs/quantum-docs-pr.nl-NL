---
uid: Microsoft.Quantum.Canon.Delay
title: Vertragings bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Delay
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: c8ba128e44a9b217ec196e39ff1df639ef276784
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840643"
---
# <a name="delay-operation"></a><span data-ttu-id="e10c8-102">Vertragings bewerking</span><span class="sxs-lookup"><span data-stu-id="e10c8-102">Delay operation</span></span>

<span data-ttu-id="e10c8-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e10c8-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e10c8-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e10c8-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e10c8-105">Hiermee wordt een bepaalde bewerking toegepast met een vertraging.</span><span class="sxs-lookup"><span data-stu-id="e10c8-105">Applies a given operation with a delay.</span></span>

```qsharp
operation Delay<'T, 'U> (op : ('T => 'U), arg : 'T, aux : Unit) : 'U
```


## <a name="description"></a><span data-ttu-id="e10c8-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e10c8-106">Description</span></span>

<span data-ttu-id="e10c8-107">Op basis van een bewerking en een invoer voor die bewerking, wordt de bewerking toegepast wanneer er extra invoer is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="e10c8-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="e10c8-108">Met name de expressie `Delay(op, arg, _)` is een bewerking die van toepassing is `op` op `arg` Wanneer aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="e10c8-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="e10c8-109">Met expressie `Delay(op,arg,_)` kan de toepassing van worden uitgesteld `op` .</span><span class="sxs-lookup"><span data-stu-id="e10c8-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="e10c8-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="e10c8-110">Input</span></span>

### <a name="op--t--u"></a><span data-ttu-id="e10c8-111">op: 'T> ' U</span><span class="sxs-lookup"><span data-stu-id="e10c8-111">op : 'T => 'U</span></span> 

<span data-ttu-id="e10c8-112">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e10c8-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="e10c8-113">arg: 'T</span><span class="sxs-lookup"><span data-stu-id="e10c8-113">arg : 'T</span></span>

<span data-ttu-id="e10c8-114">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="e10c8-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="e10c8-115">AUX: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e10c8-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="e10c8-116">Argument dat wordt gebruikt om de toepassing van de bewerking uit te stellen met behulp van een gedeeltelijke toepassing.</span><span class="sxs-lookup"><span data-stu-id="e10c8-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--u"></a><span data-ttu-id="e10c8-117">Uitvoer: ' U</span><span class="sxs-lookup"><span data-stu-id="e10c8-117">Output : 'U</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e10c8-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e10c8-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e10c8-119">T</span><span class="sxs-lookup"><span data-stu-id="e10c8-119">'T</span></span>

<span data-ttu-id="e10c8-120">Het invoer type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="e10c8-120">The input type of the operation to be delayed.</span></span>
### <a name="u"></a><span data-ttu-id="e10c8-121">' U</span><span class="sxs-lookup"><span data-stu-id="e10c8-121">'U</span></span>

<span data-ttu-id="e10c8-122">Het retour type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="e10c8-122">The return type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="e10c8-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e10c8-123">See Also</span></span>

- [<span data-ttu-id="e10c8-124">Micro soft. Quantum. Canon. DelayC</span><span class="sxs-lookup"><span data-stu-id="e10c8-124">Microsoft.Quantum.Canon.DelayC</span></span>](xref:Microsoft.Quantum.Canon.DelayC)
- [<span data-ttu-id="e10c8-125">Micro soft. Quantum. Canon. Delaya</span><span class="sxs-lookup"><span data-stu-id="e10c8-125">Microsoft.Quantum.Canon.DelayA</span></span>](xref:Microsoft.Quantum.Canon.DelayA)
- [<span data-ttu-id="e10c8-126">Micro soft. Quantum. Canon. DelayCA</span><span class="sxs-lookup"><span data-stu-id="e10c8-126">Microsoft.Quantum.Canon.DelayCA</span></span>](xref:Microsoft.Quantum.Canon.DelayCA)
- [<span data-ttu-id="e10c8-127">Micro soft. Quantum. Canon. delayed</span><span class="sxs-lookup"><span data-stu-id="e10c8-127">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)