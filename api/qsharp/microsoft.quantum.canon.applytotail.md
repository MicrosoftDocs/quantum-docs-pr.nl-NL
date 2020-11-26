---
uid: Microsoft.Quantum.Canon.ApplyToTail
title: Bewerking ApplyToTail
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTail
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 6754d41e63ea0357487fa2f62bd9209843a93347
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207969"
---
# <a name="applytotail-operation"></a><span data-ttu-id="6a084-102">Bewerking ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="6a084-102">ApplyToTail operation</span></span>

<span data-ttu-id="6a084-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6a084-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6a084-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6a084-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6a084-105">Hiermee wordt een bewerking toegepast op het laatste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="6a084-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTail<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="6a084-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6a084-106">Description</span></span>

<span data-ttu-id="6a084-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="6a084-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="6a084-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="6a084-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="6a084-109">op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6a084-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="6a084-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="6a084-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="6a084-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="6a084-111">targets : 'T[]</span></span>

<span data-ttu-id="6a084-112">Een matrix met doelen waarop de laatste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="6a084-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6a084-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6a084-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6a084-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="6a084-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6a084-115">T</span><span class="sxs-lookup"><span data-stu-id="6a084-115">'T</span></span>

<span data-ttu-id="6a084-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="6a084-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a084-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6a084-117">See Also</span></span>

- [<span data-ttu-id="6a084-118">Micro soft. Quantum. Canon. ApplyToTailA</span><span class="sxs-lookup"><span data-stu-id="6a084-118">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="6a084-119">Micro soft. Quantum. Canon. ApplyToTailC</span><span class="sxs-lookup"><span data-stu-id="6a084-119">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)
- [<span data-ttu-id="6a084-120">Micro soft. Quantum. Canon. ApplyToTailCA</span><span class="sxs-lookup"><span data-stu-id="6a084-120">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)