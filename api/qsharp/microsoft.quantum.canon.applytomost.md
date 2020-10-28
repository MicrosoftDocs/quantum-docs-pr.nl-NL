---
uid: Microsoft.Quantum.Canon.ApplyToMost
title: Bewerking ApplyToMost
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMost
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 2c6c8873859439e71436f6beb0de40dfd1e21f43
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704773"
---
# <a name="applytomost-operation"></a><span data-ttu-id="5413f-102">Bewerking ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="5413f-102">ApplyToMost operation</span></span>

<span data-ttu-id="5413f-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="5413f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="5413f-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="5413f-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="5413f-105">Hiermee wordt een bewerking toegepast op alle, behalve het laatste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="5413f-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMost<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="5413f-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="5413f-106">Description</span></span>

<span data-ttu-id="5413f-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="5413f-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="5413f-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="5413f-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="5413f-109">op: ' [] => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5413f-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="5413f-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="5413f-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="5413f-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="5413f-111">targets : 'T[]</span></span>

<span data-ttu-id="5413f-112">Een matrix met doelen, waarvan alles behalve de laatste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="5413f-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="5413f-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="5413f-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="5413f-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="5413f-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="5413f-115">T</span><span class="sxs-lookup"><span data-stu-id="5413f-115">'T</span></span>

<span data-ttu-id="5413f-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="5413f-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="5413f-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5413f-117">See Also</span></span>

- [<span data-ttu-id="5413f-118">Micro soft. Quantum. Canon. ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="5413f-118">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="5413f-119">Micro soft. Quantum. Canon. ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="5413f-119">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="5413f-120">Micro soft. Quantum. Canon. ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="5413f-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)