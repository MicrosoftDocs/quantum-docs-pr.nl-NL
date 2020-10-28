---
uid: Microsoft.Quantum.Canon.ApplyToHead
title: Bewerking ApplyToHead
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToHead
qsharp.summary: Applies an operation to the first element of an array.
ms.openlocfilehash: 4e5fc439f48a5c7e527b7805c35cce18eca3ab36
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704797"
---
# <a name="applytohead-operation"></a><span data-ttu-id="d5fa9-102">Bewerking ApplyToHead</span><span class="sxs-lookup"><span data-stu-id="d5fa9-102">ApplyToHead operation</span></span>

<span data-ttu-id="d5fa9-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="d5fa9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="d5fa9-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d5fa9-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d5fa9-105">Hiermee wordt een bewerking toegepast op het eerste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="d5fa9-105">Applies an operation to the first element of an array.</span></span>

```qsharp
operation ApplyToHead<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="d5fa9-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="d5fa9-106">Description</span></span>

<span data-ttu-id="d5fa9-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Head(targets))` .</span><span class="sxs-lookup"><span data-stu-id="d5fa9-107">Given an operation `op` and an array of targets `targets`, applies `op(Head(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="d5fa9-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="d5fa9-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="d5fa9-109">op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d5fa9-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="d5fa9-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="d5fa9-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="d5fa9-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="d5fa9-111">targets : 'T[]</span></span>

<span data-ttu-id="d5fa9-112">Een matrix met doelen waarop de eerste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="d5fa9-112">An array of targets, of which the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d5fa9-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d5fa9-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="d5fa9-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="d5fa9-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="d5fa9-115">T</span><span class="sxs-lookup"><span data-stu-id="d5fa9-115">'T</span></span>

<span data-ttu-id="d5fa9-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="d5fa9-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="d5fa9-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d5fa9-117">See Also</span></span>

- [<span data-ttu-id="d5fa9-118">Micro soft. Quantum. Canon. ApplyToHeadA</span><span class="sxs-lookup"><span data-stu-id="d5fa9-118">Microsoft.Quantum.Canon.ApplyToHeadA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadA)
- [<span data-ttu-id="d5fa9-119">Micro soft. Quantum. Canon. ApplyToHeadC</span><span class="sxs-lookup"><span data-stu-id="d5fa9-119">Microsoft.Quantum.Canon.ApplyToHeadC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadC)
- [<span data-ttu-id="d5fa9-120">Micro soft. Quantum. Canon. ApplyToHeadCA</span><span class="sxs-lookup"><span data-stu-id="d5fa9-120">Microsoft.Quantum.Canon.ApplyToHeadCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToHeadCA)