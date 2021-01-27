---
uid: Microsoft.Quantum.Canon.ApplyToTailCA
title: Bewerking ApplyToTailCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailCA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 4c702a9d310adae7a4ec404f3cf12893547623b0
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841202"
---
# <a name="applytotailca-operation"></a><span data-ttu-id="ab7b6-102">Bewerking ApplyToTailCA</span><span class="sxs-lookup"><span data-stu-id="ab7b6-102">ApplyToTailCA operation</span></span>

<span data-ttu-id="ab7b6-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ab7b6-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ab7b6-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ab7b6-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ab7b6-105">Hiermee wordt een bewerking toegepast op het laatste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="ab7b6-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="ab7b6-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ab7b6-106">Description</span></span>

<span data-ttu-id="ab7b6-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="ab7b6-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="ab7b6-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="ab7b6-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="ab7b6-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="ab7b6-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="ab7b6-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="ab7b6-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="ab7b6-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="ab7b6-111">targets : 'T[]</span></span>

<span data-ttu-id="ab7b6-112">Een matrix met doelen waarop de laatste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="ab7b6-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ab7b6-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ab7b6-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ab7b6-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="ab7b6-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ab7b6-115">T</span><span class="sxs-lookup"><span data-stu-id="ab7b6-115">'T</span></span>

<span data-ttu-id="ab7b6-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="ab7b6-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab7b6-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ab7b6-117">See Also</span></span>

- [<span data-ttu-id="ab7b6-118">Micro soft. Quantum. Canon. ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="ab7b6-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="ab7b6-119">Micro soft. Quantum. Canon. ApplyToTailA</span><span class="sxs-lookup"><span data-stu-id="ab7b6-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="ab7b6-120">Micro soft. Quantum. Canon. ApplyToTailC</span><span class="sxs-lookup"><span data-stu-id="ab7b6-120">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)