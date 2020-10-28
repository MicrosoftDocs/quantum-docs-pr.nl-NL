---
uid: Microsoft.Quantum.Canon.ApplyToElementC
title: Bewerking ApplyToElementC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementC
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: bd466ff59e6e962be9a7e58b6d298c60b0d1d90d
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704901"
---
# <a name="applytoelementc-operation"></a><span data-ttu-id="45917-102">Bewerking ApplyToElementC</span><span class="sxs-lookup"><span data-stu-id="45917-102">ApplyToElementC operation</span></span>

<span data-ttu-id="45917-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="45917-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="45917-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="45917-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="45917-105">Hiermee wordt een bewerking toegepast op een bepaald element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="45917-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementC<'T> (op : ('T => Unit is Ctl), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="45917-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="45917-106">Description</span></span>

<span data-ttu-id="45917-107">Op basis van een bewerking `op` , een index `index` en een matrix met doelen `targets` is van toepassing `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="45917-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="45917-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="45917-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="45917-109">op: 'T => CTL- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="45917-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="45917-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="45917-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="45917-111">index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="45917-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="45917-112">Een index in de matrix met doelen.</span><span class="sxs-lookup"><span data-stu-id="45917-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="45917-113">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="45917-113">targets : 'T[]</span></span>

<span data-ttu-id="45917-114">Een matrix met mogelijke doelen voor `op` .</span><span class="sxs-lookup"><span data-stu-id="45917-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="45917-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="45917-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="45917-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="45917-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="45917-117">T</span><span class="sxs-lookup"><span data-stu-id="45917-117">'T</span></span>

<span data-ttu-id="45917-118">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="45917-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="45917-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="45917-119">See Also</span></span>

- [<span data-ttu-id="45917-120">Micro soft. Quantum. Canon. ApplyToElement</span><span class="sxs-lookup"><span data-stu-id="45917-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="45917-121">Micro soft. Quantum. Canon. ApplyToElementA</span><span class="sxs-lookup"><span data-stu-id="45917-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="45917-122">Micro soft. Quantum. Canon. ApplyToElementCA</span><span class="sxs-lookup"><span data-stu-id="45917-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)