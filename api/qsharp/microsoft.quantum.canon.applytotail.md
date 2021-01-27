---
uid: Microsoft.Quantum.Canon.ApplyToTail
title: Bewerking ApplyToTail
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToTail
qsharp.summary: Applies an operation to the last element of an array.
ms.openlocfilehash: 077e6dedee68b0bd05a668387b22f8bec87a4041
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850442"
---
# <a name="applytotail-operation"></a><span data-ttu-id="71559-102">Bewerking ApplyToTail</span><span class="sxs-lookup"><span data-stu-id="71559-102">ApplyToTail operation</span></span>

<span data-ttu-id="71559-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="71559-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="71559-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="71559-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="71559-105">Hiermee wordt een bewerking toegepast op het laatste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="71559-105">Applies an operation to the last element of an array.</span></span>

```qsharp
operation ApplyToTail<'T> (op : ('T => Unit), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="71559-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="71559-106">Description</span></span>

<span data-ttu-id="71559-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Tail(targets))` .</span><span class="sxs-lookup"><span data-stu-id="71559-107">Given an operation `op` and an array of targets `targets`, applies `op(Tail(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="71559-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="71559-108">Input</span></span>

### <a name="op--t--unit"></a><span data-ttu-id="71559-109">op: 'T> [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="71559-109">op : 'T => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="71559-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="71559-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="71559-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="71559-111">targets : 'T[]</span></span>

<span data-ttu-id="71559-112">Een matrix met doelen waarop de laatste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="71559-112">An array of targets, of which the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="71559-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="71559-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="71559-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="71559-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="71559-115">T</span><span class="sxs-lookup"><span data-stu-id="71559-115">'T</span></span>

<span data-ttu-id="71559-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="71559-116">The input type of the operation to be applied.</span></span>

## <a name="example"></a><span data-ttu-id="71559-117">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="71559-117">Example</span></span>

<span data-ttu-id="71559-118">De volgende Q #-fragmenten zijn gelijk:</span><span class="sxs-lookup"><span data-stu-id="71559-118">The following Q# snippets are equivalent:</span></span>

```qsharp
ApplyToTail(H, register);
H(Tail(register));
```

## <a name="see-also"></a><span data-ttu-id="71559-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="71559-119">See Also</span></span>

- [<span data-ttu-id="71559-120">Micro soft. Quantum. Canon. ApplyToTailA</span><span class="sxs-lookup"><span data-stu-id="71559-120">Microsoft.Quantum.Canon.ApplyToTailA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailA)
- [<span data-ttu-id="71559-121">Micro soft. Quantum. Canon. ApplyToTailC</span><span class="sxs-lookup"><span data-stu-id="71559-121">Microsoft.Quantum.Canon.ApplyToTailC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailC)
- [<span data-ttu-id="71559-122">Micro soft. Quantum. Canon. ApplyToTailCA</span><span class="sxs-lookup"><span data-stu-id="71559-122">Microsoft.Quantum.Canon.ApplyToTailCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToTailCA)