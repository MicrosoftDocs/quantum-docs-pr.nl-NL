---
uid: Microsoft.Quantum.Canon.ApplyToTailCA
title: Bewerking ApplyToTailCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTailCA
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 00755df80981a09ddfd8327ee9b35761d30af4f7
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704612"
---
# <a name="applytotailca-operation"></a><span data-ttu-id="67d97-102">Bewerking ApplyToTailCA</span><span class="sxs-lookup"><span data-stu-id="67d97-102">ApplyToTailCA operation</span></span>

<span data-ttu-id="67d97-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="67d97-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="67d97-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="67d97-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="67d97-105">Hiermee wordt een bewerking toegepast op het laatste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="67d97-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTailCA<'T> (op : ('T => Unit is Adj + Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="67d97-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="67d97-106">Description</span></span>

<span data-ttu-id="67d97-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="67d97-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="67d97-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="67d97-108">Input</span></span>

### <a name="op--t--unit-adj--ctl"></a><span data-ttu-id="67d97-109">op: 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="67d97-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="67d97-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="67d97-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="67d97-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="67d97-111">targets : 'T[]</span></span>

<span data-ttu-id="67d97-112">Een matrix met doelen waarop de laatste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="67d97-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="67d97-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="67d97-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="67d97-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="67d97-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="67d97-115">T</span><span class="sxs-lookup"><span data-stu-id="67d97-115">'T</span></span>

<span data-ttu-id="67d97-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="67d97-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="67d97-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="67d97-117">See Also</span></span>

- [<span data-ttu-id="67d97-118">Micro soft. Quantum. Canon. ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="67d97-118">Microsoft.Quantum.Canon.ApplyToTail</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTail)
- [<span data-ttu-id="67d97-119">Micro soft. Quantum. Canon. ApplyToTailA</span><span class="sxs-lookup"><span data-stu-id="67d97-119">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="67d97-120">Micro soft. Quantum. Canon. ApplyToTailC</span><span class="sxs-lookup"><span data-stu-id="67d97-120">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)