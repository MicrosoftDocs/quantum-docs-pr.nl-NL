---
uid: Microsoft.Quantum.Canon.ApplyToRestCA
title: Bewerking ApplyToRestCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestCA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 3123c7f7b5e5c7f5cb17a34eedc81b3912109883
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208156"
---
# <a name="applytorestca-operation"></a><span data-ttu-id="676da-102">Bewerking ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="676da-102">ApplyToRestCA operation</span></span>

<span data-ttu-id="676da-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="676da-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="676da-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="676da-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="676da-105">Hiermee wordt een bewerking toegepast op alle, behalve het eerste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="676da-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="676da-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="676da-106">Description</span></span>

<span data-ttu-id="676da-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="676da-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="676da-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="676da-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="676da-109">op: 'T [] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="676da-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="676da-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="676da-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="676da-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="676da-111">targets : 'T[]</span></span>

<span data-ttu-id="676da-112">Een matrix met doelen, waarvan alles behalve de eerste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="676da-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="676da-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="676da-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="676da-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="676da-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="676da-115">T</span><span class="sxs-lookup"><span data-stu-id="676da-115">'T</span></span>

<span data-ttu-id="676da-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="676da-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="676da-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="676da-117">See Also</span></span>

- [<span data-ttu-id="676da-118">Micro soft. Quantum. Canon. ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="676da-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="676da-119">Micro soft. Quantum. Canon. ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="676da-119">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="676da-120">Micro soft. Quantum. Canon. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="676da-120">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)