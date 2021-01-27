---
uid: Microsoft.Quantum.Canon.ApplyToMostCA
title: Bewerking ApplyToMostCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostCA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: 0a80c23e0c6ff45083c192579dd8301d2277cef2
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841319"
---
# <a name="applytomostca-operation"></a><span data-ttu-id="6b855-102">Bewerking ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="6b855-102">ApplyToMostCA operation</span></span>

<span data-ttu-id="6b855-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6b855-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6b855-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6b855-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6b855-105">Hiermee wordt een bewerking toegepast op alle, behalve het laatste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="6b855-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostCA<'T> (op : ('T[] => Unit is Adj + Ctl), targets : 'T[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="6b855-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6b855-106">Description</span></span>

<span data-ttu-id="6b855-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="6b855-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="6b855-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="6b855-108">Input</span></span>

### <a name="op--t--unit--is-adj--ctl"></a><span data-ttu-id="6b855-109">op: 'T [] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="6b855-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="6b855-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="6b855-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="6b855-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="6b855-111">targets : 'T[]</span></span>

<span data-ttu-id="6b855-112">Een matrix met doelen, waarvan alles behalve de laatste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="6b855-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6b855-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6b855-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6b855-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="6b855-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6b855-115">T</span><span class="sxs-lookup"><span data-stu-id="6b855-115">'T</span></span>

<span data-ttu-id="6b855-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="6b855-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b855-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6b855-117">See Also</span></span>

- [<span data-ttu-id="6b855-118">Micro soft. Quantum. Canon. ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="6b855-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="6b855-119">Micro soft. Quantum. Canon. ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="6b855-119">Microsoft.Quantum.Canon.ApplyToMostA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostA)
- [<span data-ttu-id="6b855-120">Micro soft. Quantum. Canon. ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="6b855-120">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)