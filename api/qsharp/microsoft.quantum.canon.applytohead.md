---
uid: Microsoft.Quantum.Canon.ApplyToHead
title: Bewerking ApplyToHead
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHead
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 4e627b467e9354e774c2ead8b89ddd3ff3a42ef7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841325"
---
# <a name="applytohead-operation"></a><span data-ttu-id="8e1cd-102">Bewerking ApplyToHead</span><span class="sxs-lookup"><span data-stu-id="8e1cd-102">ApplyToHead operation</span></span>

<span data-ttu-id="8e1cd-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8e1cd-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8e1cd-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8e1cd-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8e1cd-105">Hiermee wordt een bewerking toegepast op het eerste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="8e1cd-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHead<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="8e1cd-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8e1cd-106">Description</span></span>

<span data-ttu-id="8e1cd-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="8e1cd-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="8e1cd-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="8e1cd-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="8e1cd-109">op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8e1cd-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="8e1cd-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="8e1cd-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="8e1cd-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="8e1cd-111">targets : 'T[]</span></span>

<span data-ttu-id="8e1cd-112">Een matrix met doelen waarop de eerste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="8e1cd-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8e1cd-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8e1cd-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="8e1cd-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="8e1cd-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="8e1cd-115">T</span><span class="sxs-lookup"><span data-stu-id="8e1cd-115">'T</span></span>

<span data-ttu-id="8e1cd-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="8e1cd-116">The input type of the operation to be applied.</span></span>

## <a name="example"></a><span data-ttu-id="8e1cd-117">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="8e1cd-117">Example</span></span>

<span data-ttu-id="8e1cd-118">De volgende Q #-fragmenten zijn gelijk:</span><span class="sxs-lookup"><span data-stu-id="8e1cd-118">The following Q# snippets are equivalent:</span></span>

```qsharp
ApplyToHead(H, register);
H(Head(register));
```

## <a name="see-also"></a><span data-ttu-id="8e1cd-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8e1cd-119">See Also</span></span>

- [<span data-ttu-id="8e1cd-120">Micro soft. Quantum. Canon. ApplyToHeadA</span><span class="sxs-lookup"><span data-stu-id="8e1cd-120">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="8e1cd-121">Micro soft. Quantum. Canon. ApplyToHeadC</span><span class="sxs-lookup"><span data-stu-id="8e1cd-121">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="8e1cd-122">Micro soft. Quantum. Canon. ApplyToHeadCA</span><span class="sxs-lookup"><span data-stu-id="8e1cd-122">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)