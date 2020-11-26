---
uid: Microsoft.Quantum.Canon.ApplyToMostA
title: Bewerking ApplyToMostA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 7c226de9b2c99d124c467175dfe65a60a89d4332
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208496"
---
# <a name="applytomosta-operation"></a><span data-ttu-id="10936-102">Bewerking ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="10936-102">ApplyToMostA operation</span></span>

<span data-ttu-id="10936-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="10936-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="10936-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="10936-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="10936-105">Hiermee wordt een bewerking toegepast op alle, behalve het laatste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="10936-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="10936-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="10936-106">Description</span></span>

<span data-ttu-id="10936-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="10936-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="10936-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="10936-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="10936-109">op: 'T [] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="10936-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="10936-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="10936-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="10936-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="10936-111">targets : 'T[]</span></span>

<span data-ttu-id="10936-112">Een matrix met doelen, waarvan alles behalve de laatste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="10936-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="10936-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="10936-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="10936-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="10936-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="10936-115">T</span><span class="sxs-lookup"><span data-stu-id="10936-115">'T</span></span>

<span data-ttu-id="10936-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="10936-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="10936-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="10936-117">See Also</span></span>

- [<span data-ttu-id="10936-118">Micro soft. Quantum. Canon. ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="10936-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="10936-119">Micro soft. Quantum. Canon. ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="10936-119">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="10936-120">Micro soft. Quantum. Canon. ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="10936-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)