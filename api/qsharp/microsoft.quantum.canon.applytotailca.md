---
uid: Microsoft.Quantum.Canon.ApplyToTailCA
title: Bewerking ApplyToTailCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailCA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: afb9eaa277814d7434b00a5c853a0c002190c1ae
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207850"
---
# <a name="applytotailca-operation"></a><span data-ttu-id="e28cc-102">Bewerking ApplyToTailCA</span><span class="sxs-lookup"><span data-stu-id="e28cc-102">ApplyToTailCA operation</span></span>

<span data-ttu-id="e28cc-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e28cc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e28cc-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e28cc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e28cc-105">Hiermee wordt een bewerking toegepast op het laatste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="e28cc-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="e28cc-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e28cc-106">Description</span></span>

<span data-ttu-id="e28cc-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="e28cc-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="e28cc-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="e28cc-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="e28cc-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="e28cc-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="e28cc-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e28cc-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="e28cc-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="e28cc-111">targets : 'T[]</span></span>

<span data-ttu-id="e28cc-112">Een matrix met doelen waarop de laatste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="e28cc-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e28cc-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e28cc-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e28cc-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e28cc-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e28cc-115">T</span><span class="sxs-lookup"><span data-stu-id="e28cc-115">'T</span></span>

<span data-ttu-id="e28cc-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e28cc-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="e28cc-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e28cc-117">See Also</span></span>

- [<span data-ttu-id="e28cc-118">Micro soft. Quantum. Canon. ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="e28cc-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="e28cc-119">Micro soft. Quantum. Canon. ApplyToTailA</span><span class="sxs-lookup"><span data-stu-id="e28cc-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="e28cc-120">Micro soft. Quantum. Canon. ApplyToTailC</span><span class="sxs-lookup"><span data-stu-id="e28cc-120">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)