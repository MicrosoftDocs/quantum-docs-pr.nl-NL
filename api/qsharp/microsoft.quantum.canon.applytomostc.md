---
uid: Microsoft.Quantum.Canon.ApplyToMostC
title: Bewerking ApplyToMostC
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostC
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: af55093e44ce023c9e8b7e478730f4c527cf6d32
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208462"
---
# <a name="applytomostc-operation"></a><span data-ttu-id="ce932-102">Bewerking ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="ce932-102">ApplyToMostC operation</span></span>

<span data-ttu-id="ce932-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ce932-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ce932-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ce932-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ce932-105">Hiermee wordt een bewerking toegepast op alle, behalve het laatste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="ce932-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit is Ctl
```


## <a name="description"></a><span data-ttu-id="ce932-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ce932-106">Description</span></span>

<span data-ttu-id="ce932-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="ce932-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="ce932-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="ce932-108">Input</span></span>

### <a name="op--t--unit--is-ctl"></a><span data-ttu-id="ce932-109">op: 'T [] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="ce932-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="ce932-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="ce932-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="ce932-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="ce932-111">targets : 'T[]</span></span>

<span data-ttu-id="ce932-112">Een matrix met doelen, waarvan alles behalve de laatste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="ce932-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ce932-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ce932-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="ce932-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="ce932-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="ce932-115">T</span><span class="sxs-lookup"><span data-stu-id="ce932-115">'T</span></span>

<span data-ttu-id="ce932-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="ce932-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="ce932-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ce932-117">See Also</span></span>

- [<span data-ttu-id="ce932-118">Micro soft. Quantum. Canon. ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="ce932-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="ce932-119">Micro soft. Quantum. Canon. ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="ce932-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="ce932-120">Micro soft. Quantum. Canon. ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="ce932-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)