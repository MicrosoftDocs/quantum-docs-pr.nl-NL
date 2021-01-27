---
uid: Microsoft.Quantum.Canon.ApplyToMost
title: Bewerking ApplyToMost
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMost
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: a3918233e101f3d8956601dcc7d85edcf6196ac7
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850593"
---
# <a name="applytomost-operation"></a><span data-ttu-id="aef42-102">Bewerking ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="aef42-102">ApplyToMost operation</span></span>

<span data-ttu-id="aef42-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="aef42-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="aef42-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="aef42-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="aef42-105">Hiermee wordt een bewerking toegepast op alle, behalve het laatste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="aef42-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMost<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="aef42-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="aef42-106">Description</span></span>

<span data-ttu-id="aef42-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="aef42-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="aef42-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="aef42-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="aef42-109">op: ' [] => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="aef42-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="aef42-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="aef42-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="aef42-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="aef42-111">targets : 'T[]</span></span>

<span data-ttu-id="aef42-112">Een matrix met doelen, waarvan alles behalve de laatste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="aef42-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="aef42-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="aef42-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="aef42-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="aef42-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="aef42-115">T</span><span class="sxs-lookup"><span data-stu-id="aef42-115">'T</span></span>

<span data-ttu-id="aef42-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="aef42-116">The input type of the operation to be applied.</span></span>

## <a name="example"></a><span data-ttu-id="aef42-117">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="aef42-117">Example</span></span>

<span data-ttu-id="aef42-118">De volgende Q #-fragmenten zijn gelijk:</span><span class="sxs-lookup"><span data-stu-id="aef42-118">The following Q# snippets are equivalent:</span></span>

```qsharp
ApplyToMost(ApplyCNOTChain, register);
ApplyCNOTChain(Most(register));
```

## <a name="see-also"></a><span data-ttu-id="aef42-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="aef42-119">See Also</span></span>

- [<span data-ttu-id="aef42-120">Micro soft. Quantum. Canon. ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="aef42-120">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="aef42-121">Micro soft. Quantum. Canon. ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="aef42-121">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="aef42-122">Micro soft. Quantum. Canon. ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="aef42-122">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)