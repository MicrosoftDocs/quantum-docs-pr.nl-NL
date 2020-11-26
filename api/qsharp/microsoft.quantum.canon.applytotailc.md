---
uid: Microsoft.Quantum.Canon.ApplyToTailC
title: Bewerking ApplyToTailC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailC
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 5a68cae3fd122416cfd064e0078e03f5c00ab492
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96217285"
---
# <a name="applytotailc-operation"></a><span data-ttu-id="e1516-102">Bewerking ApplyToTailC</span><span class="sxs-lookup"><span data-stu-id="e1516-102">ApplyToTailC operation</span></span>

<span data-ttu-id="e1516-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e1516-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e1516-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="e1516-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="e1516-105">Hiermee wordt een bewerking toegepast op het laatste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="e1516-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailC<'T> (op : ('T => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="e1516-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e1516-106">Description</span></span>

<span data-ttu-id="e1516-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="e1516-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="e1516-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="e1516-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="e1516-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="e1516-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="e1516-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e1516-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="e1516-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="e1516-111">targets : 'T[]</span></span>

<span data-ttu-id="e1516-112">Een matrix met doelen waarop de laatste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="e1516-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e1516-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e1516-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e1516-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e1516-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e1516-115">T</span><span class="sxs-lookup"><span data-stu-id="e1516-115">'T</span></span>

<span data-ttu-id="e1516-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e1516-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1516-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e1516-117">See Also</span></span>

- [<span data-ttu-id="e1516-118">Micro soft. Quantum. Canon. ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="e1516-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="e1516-119">Micro soft. Quantum. Canon. ApplyToTailA</span><span class="sxs-lookup"><span data-stu-id="e1516-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="e1516-120">Micro soft. Quantum. Canon. ApplyToTailCA</span><span class="sxs-lookup"><span data-stu-id="e1516-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)