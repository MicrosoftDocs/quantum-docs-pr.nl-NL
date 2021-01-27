---
uid: Microsoft.Quantum.Canon.DelayC
title: Bewerking DelayC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: DelayC
qsharp.summary: Applies a given operation with a delay.
ms.openlocfilehash: eba4c3bd9f472910e30e5ac8334f09471a685c5d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840640"
---
# <a name="delayc-operation"></a><span data-ttu-id="c2241-102">Bewerking DelayC</span><span class="sxs-lookup"><span data-stu-id="c2241-102">DelayC operation</span></span>

<span data-ttu-id="c2241-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c2241-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c2241-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c2241-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c2241-105">Hiermee wordt een bepaalde bewerking toegepast met een vertraging.</span><span class="sxs-lookup"><span data-stu-id="c2241-105">Applies a given operation with a delay.</span></span>

```qsharp
operation DelayC<'T> (op : ('T => Unit is Ctl), arg : 'T, aux : Unit) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="c2241-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="c2241-106">Description</span></span>

<span data-ttu-id="c2241-107">Op basis van een bewerking en een invoer voor die bewerking, wordt de bewerking toegepast wanneer er extra invoer is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="c2241-107">Given an operation and an input to that operation, applies the operation once an additional input is provided.</span></span>
<span data-ttu-id="c2241-108">Met name de expressie `Delay(op, arg, _)` is een bewerking die van toepassing is `op` op `arg` Wanneer aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="c2241-108">In particular, the expression `Delay(op, arg, _)` is an operation that applies `op` to `arg` when called.</span></span>
<span data-ttu-id="c2241-109">Met expressie `Delay(op,arg,_)` kan de toepassing van worden uitgesteld `op` .</span><span class="sxs-lookup"><span data-stu-id="c2241-109">Expression `Delay(op,arg,_)` allows to delay the application of `op`.</span></span>

## <a name="input"></a><span data-ttu-id="c2241-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="c2241-110">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="c2241-111">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="c2241-111">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="c2241-112">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="c2241-112">An operation to be applied.</span></span>


### <a name="arg--t"></a><span data-ttu-id="c2241-113">arg: 'T</span><span class="sxs-lookup"><span data-stu-id="c2241-113">arg : 'T</span></span>

<span data-ttu-id="c2241-114">De invoer waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="c2241-114">The input to which the operation is applied.</span></span>


### <a name="aux--unit"></a><span data-ttu-id="c2241-115">AUX: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c2241-115">aux : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

<span data-ttu-id="c2241-116">Argument dat wordt gebruikt om de toepassing van de bewerking uit te stellen met behulp van een gedeeltelijke toepassing.</span><span class="sxs-lookup"><span data-stu-id="c2241-116">Argument used to delay the application of operation by using partial application.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c2241-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c2241-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c2241-118">Type parameters</span><span class="sxs-lookup"><span data-stu-id="c2241-118">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c2241-119">T</span><span class="sxs-lookup"><span data-stu-id="c2241-119">'T</span></span>

<span data-ttu-id="c2241-120">Het invoer type van de bewerking die moet worden uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="c2241-120">The input type of the operation to be delayed.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2241-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c2241-121">See Also</span></span>

- [<span data-ttu-id="c2241-122">Micro soft. Quantum. Canon. delay</span><span class="sxs-lookup"><span data-stu-id="c2241-122">Microsoft.Quantum.Canon.Delay</span></span>](xref:Microsoft.Quantum.Canon.Delay)
- [<span data-ttu-id="c2241-123">Micro soft. Quantum. Canon. delayed</span><span class="sxs-lookup"><span data-stu-id="c2241-123">Microsoft.Quantum.Canon.Delayed</span></span>](xref:Microsoft.Quantum.Canon.Delayed)