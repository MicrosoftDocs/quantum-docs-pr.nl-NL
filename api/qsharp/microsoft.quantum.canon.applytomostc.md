---
uid: Microsoft.Quantum.Canon.ApplyToMostC
title: Bewerking ApplyToMostC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostC
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 14de9f367aa7d19f64f13186d402239ae1fef3c1
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850565"
---
# <a name="applytomostc-operation"></a><span data-ttu-id="42742-102">Bewerking ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="42742-102">ApplyToMostC operation</span></span>

<span data-ttu-id="42742-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="42742-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="42742-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="42742-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="42742-105">Hiermee wordt een bewerking toegepast op alle, behalve het laatste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="42742-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="42742-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="42742-106">Description</span></span>

<span data-ttu-id="42742-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="42742-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="42742-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="42742-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="42742-109">op: 'T [] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="42742-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="42742-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="42742-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="42742-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="42742-111">targets : 'T[]</span></span>

<span data-ttu-id="42742-112">Een matrix met doelen, waarvan alles behalve de laatste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="42742-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="42742-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="42742-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="42742-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="42742-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="42742-115">T</span><span class="sxs-lookup"><span data-stu-id="42742-115">'T</span></span>

<span data-ttu-id="42742-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="42742-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="42742-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="42742-117">See Also</span></span>

- [<span data-ttu-id="42742-118">Micro soft. Quantum. Canon. ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="42742-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="42742-119">Micro soft. Quantum. Canon. ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="42742-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="42742-120">Micro soft. Quantum. Canon. ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="42742-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)