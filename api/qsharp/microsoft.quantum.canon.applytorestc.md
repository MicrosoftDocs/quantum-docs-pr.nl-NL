---
uid: Microsoft.Quantum.Canon.ApplyToRestC
title: Bewerking ApplyToRestC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestC
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 1e533a9f0994b70054aeca2f9ddd97f4e200b03f
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850493"
---
# <a name="applytorestc-operation"></a><span data-ttu-id="92539-102">Bewerking ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="92539-102">ApplyToRestC operation</span></span>

<span data-ttu-id="92539-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="92539-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="92539-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="92539-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="92539-105">Hiermee wordt een bewerking toegepast op alle, behalve het eerste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="92539-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="92539-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="92539-106">Description</span></span>

<span data-ttu-id="92539-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="92539-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="92539-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="92539-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="92539-109">op: 'T [] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="92539-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="92539-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="92539-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="92539-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="92539-111">targets : 'T[]</span></span>

<span data-ttu-id="92539-112">Een matrix met doelen, waarvan alles behalve de eerste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="92539-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="92539-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="92539-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="92539-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="92539-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="92539-115">T</span><span class="sxs-lookup"><span data-stu-id="92539-115">'T</span></span>

<span data-ttu-id="92539-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="92539-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="92539-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="92539-117">See Also</span></span>

- [<span data-ttu-id="92539-118">Micro soft. Quantum. Canon. ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="92539-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="92539-119">Micro soft. Quantum. Canon. ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="92539-119">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="92539-120">Micro soft. Quantum. Canon. ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="92539-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)