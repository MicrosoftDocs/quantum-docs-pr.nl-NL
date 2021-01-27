---
uid: Microsoft.Quantum.Canon.ApplyToElementA
title: Bewerking ApplyToElementA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToElementA
qsharp.summary: Applies an operation to a given element of an array.
ms.openlocfilehash: 57d870c7fbd099212b13f75bd85e57c046280d73
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850769"
---
# <a name="applytoelementa-operation"></a><span data-ttu-id="b4d1f-102">Bewerking ApplyToElementA</span><span class="sxs-lookup"><span data-stu-id="b4d1f-102">ApplyToElementA operation</span></span>

<span data-ttu-id="b4d1f-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="b4d1f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="b4d1f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b4d1f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b4d1f-105">Hiermee wordt een bewerking toegepast op een bepaald element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="b4d1f-105">Applies an operation to a given element of an array.</span></span>

```qsharp
operation ApplyToElementA<'T> (op : ('T => Unit is Adj), index : Int, targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="b4d1f-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="b4d1f-106">Description</span></span>

<span data-ttu-id="b4d1f-107">Op basis van een bewerking `op` , een index `index` en een matrix met doelen `targets` is van toepassing `op(targets[index])` .</span><span class="sxs-lookup"><span data-stu-id="b4d1f-107">Given an operation `op`, an index `index`, and an array of targets `targets`, applies `op(targets[index])`.</span></span>

## <a name="input"></a><span data-ttu-id="b4d1f-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="b4d1f-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="b4d1f-109">op: 'T => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="b4d1f-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="b4d1f-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="b4d1f-110">An operation to be applied.</span></span>


### <a name="index--int"></a><span data-ttu-id="b4d1f-111">index: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="b4d1f-111">index : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="b4d1f-112">Een index in de matrix met doelen.</span><span class="sxs-lookup"><span data-stu-id="b4d1f-112">An index into the array of targets.</span></span>


### <a name="targets--t"></a><span data-ttu-id="b4d1f-113">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="b4d1f-113">targets : 'T[]</span></span>

<span data-ttu-id="b4d1f-114">Een matrix met mogelijke doelen voor `op` .</span><span class="sxs-lookup"><span data-stu-id="b4d1f-114">An array of possible targets for `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="b4d1f-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="b4d1f-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="b4d1f-116">Type parameters</span><span class="sxs-lookup"><span data-stu-id="b4d1f-116">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="b4d1f-117">T</span><span class="sxs-lookup"><span data-stu-id="b4d1f-117">'T</span></span>

<span data-ttu-id="b4d1f-118">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="b4d1f-118">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="b4d1f-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="b4d1f-119">See Also</span></span>

- [<span data-ttu-id="b4d1f-120">Micro soft. Quantum. Canon. ApplyToElement</span><span class="sxs-lookup"><span data-stu-id="b4d1f-120">Microsoft.Quantum.Canon.ApplyToElement</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElement)
- [<span data-ttu-id="b4d1f-121">Micro soft. Quantum. Canon. ApplyToElementC</span><span class="sxs-lookup"><span data-stu-id="b4d1f-121">Microsoft.Quantum.Canon.ApplyToElementC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementC)
- [<span data-ttu-id="b4d1f-122">Micro soft. Quantum. Canon. ApplyToElementCA</span><span class="sxs-lookup"><span data-stu-id="b4d1f-122">Microsoft.Quantum.Canon.ApplyToElementCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToElementCA)