---
uid: Microsoft.Quantum.Canon.ApplyToRest
title: Bewerking ApplyToRest
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRest
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: f18536a056935220feedc4ea50531c5def61d650
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850515"
---
# <a name="applytorest-operation"></a><span data-ttu-id="793e2-102">Bewerking ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="793e2-102">ApplyToRest operation</span></span>

<span data-ttu-id="793e2-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="793e2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="793e2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="793e2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="793e2-105">Hiermee wordt een bewerking toegepast op alle, behalve het eerste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="793e2-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRest<'T> (op : ('T[] => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="793e2-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="793e2-106">Description</span></span>

<span data-ttu-id="793e2-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="793e2-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="793e2-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="793e2-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="793e2-109">op: ' [] => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="793e2-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="793e2-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="793e2-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="793e2-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="793e2-111">targets : 'T[]</span></span>

<span data-ttu-id="793e2-112">Een matrix met doelen, waarvan alles behalve de eerste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="793e2-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="793e2-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="793e2-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="793e2-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="793e2-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="793e2-115">T</span><span class="sxs-lookup"><span data-stu-id="793e2-115">'T</span></span>

<span data-ttu-id="793e2-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="793e2-116">The input type of the operation to be applied.</span></span>

## <a name="example"></a><span data-ttu-id="793e2-117">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="793e2-117">Example</span></span>

<span data-ttu-id="793e2-118">De volgende Q #-fragmenten zijn gelijk:</span><span class="sxs-lookup"><span data-stu-id="793e2-118">The following Q# snippets are equivalent:</span></span>

```qsharp
ApplyToRest(ApplyCNOTChain, register);
ApplyCNOTChain(Rest(register));
```

## <a name="see-also"></a><span data-ttu-id="793e2-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="793e2-119">See Also</span></span>

- [<span data-ttu-id="793e2-120">Micro soft. Quantum. Canon. ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="793e2-120">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="793e2-121">Micro soft. Quantum. Canon. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="793e2-121">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="793e2-122">Micro soft. Quantum. Canon. ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="793e2-122">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)