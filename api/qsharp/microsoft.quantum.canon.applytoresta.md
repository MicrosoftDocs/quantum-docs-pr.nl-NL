---
uid: Microsoft.Quantum.Canon.ApplyToRestA
title: Bewerking ApplyToRestA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 34cb5071dd939d0831e39bb8f1670670ae1fad31
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208297"
---
# <a name="applytoresta-operation"></a><span data-ttu-id="81a36-102">Bewerking ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="81a36-102">ApplyToRestA operation</span></span>

<span data-ttu-id="81a36-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="81a36-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="81a36-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="81a36-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="81a36-105">Hiermee wordt een bewerking toegepast op alle, behalve het eerste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="81a36-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="81a36-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="81a36-106">Description</span></span>

<span data-ttu-id="81a36-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="81a36-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="81a36-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="81a36-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="81a36-109">op: 'T [] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="81a36-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="81a36-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="81a36-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="81a36-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="81a36-111">targets : 'T[]</span></span>

<span data-ttu-id="81a36-112">Een matrix met doelen, waarvan alles behalve de eerste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="81a36-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="81a36-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="81a36-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="81a36-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="81a36-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="81a36-115">T</span><span class="sxs-lookup"><span data-stu-id="81a36-115">'T</span></span>

<span data-ttu-id="81a36-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="81a36-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="81a36-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="81a36-117">See Also</span></span>

- [<span data-ttu-id="81a36-118">Micro soft. Quantum. Canon. ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="81a36-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="81a36-119">Micro soft. Quantum. Canon. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="81a36-119">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="81a36-120">Micro soft. Quantum. Canon. ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="81a36-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)