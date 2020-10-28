---
uid: Microsoft.Quantum.Canon.ApplyToMostC
title: Bewerking ApplyToMostC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostC
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: a5927f6b296dd50afec8979c8e8ac22979b8a082
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704741"
---
# <a name="applytomostc-operation"></a><span data-ttu-id="e74cc-102">Bewerking ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="e74cc-102">ApplyToMostC operation</span></span>

<span data-ttu-id="e74cc-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e74cc-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e74cc-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e74cc-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e74cc-105">Hiermee wordt een bewerking toegepast op alle, behalve het laatste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="e74cc-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="e74cc-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e74cc-106">Description</span></span>

<span data-ttu-id="e74cc-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="e74cc-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="e74cc-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="e74cc-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="e74cc-109">op: ' [] = CTL van>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e74cc-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="e74cc-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e74cc-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="e74cc-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="e74cc-111">targets : 'T[]</span></span>

<span data-ttu-id="e74cc-112">Een matrix met doelen, waarvan alles behalve de laatste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="e74cc-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e74cc-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e74cc-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e74cc-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e74cc-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e74cc-115">T</span><span class="sxs-lookup"><span data-stu-id="e74cc-115">'T</span></span>

<span data-ttu-id="e74cc-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e74cc-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="e74cc-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e74cc-117">See Also</span></span>

- [<span data-ttu-id="e74cc-118">Micro soft. Quantum. Canon. ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="e74cc-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="e74cc-119">Micro soft. Quantum. Canon. ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="e74cc-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="e74cc-120">Micro soft. Quantum. Canon. ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="e74cc-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)