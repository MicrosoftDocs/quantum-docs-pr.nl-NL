---
uid: Microsoft.Quantum.Canon.ApplyToMostCA
title: Bewerking ApplyToMostCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostCA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 797cbd835446f31b2df60dbb184f888e6d0356aa
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704740"
---
# <a name="applytomostca-operation"></a><span data-ttu-id="e71af-102">Bewerking ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="e71af-102">ApplyToMostCA operation</span></span>

<span data-ttu-id="e71af-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e71af-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e71af-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e71af-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e71af-105">Hiermee wordt een bewerking toegepast op alle, behalve het laatste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="e71af-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="e71af-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e71af-106">Description</span></span>

<span data-ttu-id="e71af-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="e71af-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="e71af-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="e71af-108">Input</span></span>

### <a name="op--t--unit-adj--ctl"></a><span data-ttu-id="e71af-109">op: 'T [] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="e71af-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="e71af-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e71af-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="e71af-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="e71af-111">targets : 'T[]</span></span>

<span data-ttu-id="e71af-112">Een matrix met doelen, waarvan alles behalve de laatste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="e71af-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e71af-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e71af-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e71af-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e71af-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e71af-115">T</span><span class="sxs-lookup"><span data-stu-id="e71af-115">'T</span></span>

<span data-ttu-id="e71af-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e71af-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="e71af-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e71af-117">See Also</span></span>

- [<span data-ttu-id="e71af-118">Micro soft. Quantum. Canon. ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="e71af-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="e71af-119">Micro soft. Quantum. Canon. ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="e71af-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="e71af-120">Micro soft. Quantum. Canon. ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="e71af-120">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)