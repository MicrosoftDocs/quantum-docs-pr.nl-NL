---
uid: Microsoft.Quantum.Canon.ApplyToElement
title: Bewerking ApplyToElement
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElement
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 5c321d95c9b79bc50827c2b50c406b164e143dc6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704933"
---
# <a name="applytoelement-operation"></a><span data-ttu-id="e8c8b-102">Bewerking ApplyToElement</span><span class="sxs-lookup"><span data-stu-id="e8c8b-102">ApplyToElement operation</span></span>

<span data-ttu-id="e8c8b-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e8c8b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e8c8b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e8c8b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e8c8b-105">Hiermee wordt een bewerking toegepast op een bepaald element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="e8c8b-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElement<'T> (op : ('T => Unit), index : Int, targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="e8c8b-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e8c8b-106">Description</span></span>

<span data-ttu-id="e8c8b-107">Op basis van een bewerking `op` , een index `index` en een matrix met doelen `targets` is van toepassing `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="e8c8b-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="e8c8b-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="e8c8b-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="e8c8b-109">op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e8c8b-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="e8c8b-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e8c8b-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="e8c8b-111">index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e8c8b-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e8c8b-112">Een index in de matrix met doelen.</span><span class="sxs-lookup"><span data-stu-id="e8c8b-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="e8c8b-113">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="e8c8b-113">targets : 'T[]</span></span>

<span data-ttu-id="e8c8b-114">Een matrix met mogelijke doelen voor `op` .</span><span class="sxs-lookup"><span data-stu-id="e8c8b-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e8c8b-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e8c8b-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e8c8b-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e8c8b-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="e8c8b-117">T</span><span class="sxs-lookup"><span data-stu-id="e8c8b-117">'T</span></span>

<span data-ttu-id="e8c8b-118">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="e8c8b-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="e8c8b-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e8c8b-119">See Also</span></span>

- [<span data-ttu-id="e8c8b-120">Micro soft. Quantum. Canon. ApplyToElementC</span><span class="sxs-lookup"><span data-stu-id="e8c8b-120">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="e8c8b-121">Micro soft. Quantum. Canon. ApplyToElementA</span><span class="sxs-lookup"><span data-stu-id="e8c8b-121">Microsoft.Quantum.Canon.ApplyToElementA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementA)
- [<span data-ttu-id="e8c8b-122">Micro soft. Quantum. Canon. ApplyToElementCA</span><span class="sxs-lookup"><span data-stu-id="e8c8b-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)