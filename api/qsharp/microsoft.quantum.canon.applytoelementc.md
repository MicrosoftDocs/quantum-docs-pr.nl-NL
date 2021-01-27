---
uid: Microsoft.Quantum.Canon.ApplyToElementC
title: Bewerking ApplyToElementC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementC
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: bc63b6b591781a6283b872ef0c2509094a656b4c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850748"
---
# <a name="applytoelementc-operation"></a><span data-ttu-id="aa8e1-102">Bewerking ApplyToElementC</span><span class="sxs-lookup"><span data-stu-id="aa8e1-102">ApplyToElementC operation</span></span>

<span data-ttu-id="aa8e1-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="aa8e1-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="aa8e1-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aa8e1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aa8e1-105">Hiermee wordt een bewerking toegepast op een bepaald element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="aa8e1-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementC<'T> (op : ('T => Unit is Ctl), index : Int, targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="aa8e1-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="aa8e1-106">Description</span></span>

<span data-ttu-id="aa8e1-107">Op basis van een bewerking `op` , een index `index` en een matrix met doelen `targets` is van toepassing `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="aa8e1-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="aa8e1-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="aa8e1-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="aa8e1-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="aa8e1-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="aa8e1-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="aa8e1-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="aa8e1-111">index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="aa8e1-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="aa8e1-112">Een index in de matrix met doelen.</span><span class="sxs-lookup"><span data-stu-id="aa8e1-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="aa8e1-113">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="aa8e1-113">targets : 'T[]</span></span>

<span data-ttu-id="aa8e1-114">Een matrix met mogelijke doelen voor `op` .</span><span class="sxs-lookup"><span data-stu-id="aa8e1-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="aa8e1-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="aa8e1-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="aa8e1-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="aa8e1-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="aa8e1-117">T</span><span class="sxs-lookup"><span data-stu-id="aa8e1-117">'T</span></span>

<span data-ttu-id="aa8e1-118">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="aa8e1-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="aa8e1-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="aa8e1-119">See Also</span></span>

- [<span data-ttu-id="aa8e1-120">Micro soft. Quantum. Canon. ApplyToElement</span><span class="sxs-lookup"><span data-stu-id="aa8e1-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="aa8e1-121">Micro soft. Quantum. Canon. ApplyToElementA</span><span class="sxs-lookup"><span data-stu-id="aa8e1-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="aa8e1-122">Micro soft. Quantum. Canon. ApplyToElementCA</span><span class="sxs-lookup"><span data-stu-id="aa8e1-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)