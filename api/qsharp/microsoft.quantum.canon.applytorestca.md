---
uid: Microsoft.Quantum.Canon.ApplyToRestCA
title: Bewerking ApplyToRestCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestCA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: d2dc10803044980d53f80f0577d16cb14a2eb301
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704684"
---
# <a name="applytorestca-operation"></a><span data-ttu-id="8b0c2-102">Bewerking ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="8b0c2-102">ApplyToRestCA operation</span></span>

<span data-ttu-id="8b0c2-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8b0c2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8b0c2-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="8b0c2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="8b0c2-105">Hiermee wordt een bewerking toegepast op alle, behalve het eerste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="8b0c2-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="8b0c2-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8b0c2-106">Description</span></span>

<span data-ttu-id="8b0c2-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="8b0c2-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="8b0c2-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="8b0c2-108">Input</span></span>

### <a name="op--t--unit-adj--ctl"></a><span data-ttu-id="8b0c2-109">op: 'T [] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="8b0c2-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="8b0c2-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="8b0c2-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="8b0c2-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="8b0c2-111">targets : 'T[]</span></span>

<span data-ttu-id="8b0c2-112">Een matrix met doelen, waarvan alles behalve de eerste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="8b0c2-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8b0c2-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8b0c2-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8b0c2-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="8b0c2-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8b0c2-115">T</span><span class="sxs-lookup"><span data-stu-id="8b0c2-115">'T</span></span>

<span data-ttu-id="8b0c2-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="8b0c2-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="8b0c2-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8b0c2-117">See Also</span></span>

- [<span data-ttu-id="8b0c2-118">Micro soft. Quantum. Canon. ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="8b0c2-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="8b0c2-119">Micro soft. Quantum. Canon. ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="8b0c2-119">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="8b0c2-120">Micro soft. Quantum. Canon. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="8b0c2-120">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)