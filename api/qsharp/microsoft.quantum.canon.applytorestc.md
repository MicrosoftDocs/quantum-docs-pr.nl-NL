---
uid: Microsoft.Quantum.Canon.ApplyToRestC
title: Bewerking ApplyToRestC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestC
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 55e534b7b7673f300b607a8213418c45c8c7c92c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704700"
---
# <a name="applytorestc-operation"></a><span data-ttu-id="f8f67-102">Bewerking ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="f8f67-102">ApplyToRestC operation</span></span>

<span data-ttu-id="f8f67-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f8f67-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f8f67-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="f8f67-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="f8f67-105">Hiermee wordt een bewerking toegepast op alle, behalve het eerste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="f8f67-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestC<'T> (op : ('T[] => Unit is Ctl), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="f8f67-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f8f67-106">Description</span></span>

<span data-ttu-id="f8f67-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="f8f67-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="f8f67-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="f8f67-108">Input</span></span>

### <a name="op--t--unit-ctl"></a><span data-ttu-id="f8f67-109">op: ' [] = CTL van>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f8f67-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="f8f67-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="f8f67-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="f8f67-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="f8f67-111">targets : 'T[]</span></span>

<span data-ttu-id="f8f67-112">Een matrix met doelen, waarvan alles behalve de eerste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="f8f67-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f8f67-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f8f67-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="f8f67-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="f8f67-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f8f67-115">T</span><span class="sxs-lookup"><span data-stu-id="f8f67-115">'T</span></span>

<span data-ttu-id="f8f67-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="f8f67-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8f67-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f8f67-117">See Also</span></span>

- [<span data-ttu-id="f8f67-118">Micro soft. Quantum. Canon. ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="f8f67-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="f8f67-119">Micro soft. Quantum. Canon. ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="f8f67-119">Microsoft.Quantum.Canon.ApplyToRestA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestA)
- [<span data-ttu-id="f8f67-120">Micro soft. Quantum. Canon. ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="f8f67-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)