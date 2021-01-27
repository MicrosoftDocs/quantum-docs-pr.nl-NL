---
uid: Microsoft.Quantum.Canon.ApplyToRestA
title: Bewerking ApplyToRestA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 69001f6c8d65806e7259f2d2f2741d48866daa84
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841269"
---
# <a name="applytoresta-operation"></a><span data-ttu-id="26a59-102">Bewerking ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="26a59-102">ApplyToRestA operation</span></span>

<span data-ttu-id="26a59-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="26a59-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="26a59-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="26a59-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="26a59-105">Hiermee wordt een bewerking toegepast op alle, behalve het eerste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="26a59-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="26a59-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="26a59-106">Description</span></span>

<span data-ttu-id="26a59-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="26a59-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="26a59-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="26a59-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="26a59-109">op: 'T [] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="26a59-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="26a59-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="26a59-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="26a59-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="26a59-111">targets : 'T[]</span></span>

<span data-ttu-id="26a59-112">Een matrix met doelen, waarvan alles behalve de eerste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="26a59-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="26a59-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="26a59-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="26a59-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="26a59-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="26a59-115">T</span><span class="sxs-lookup"><span data-stu-id="26a59-115">'T</span></span>

<span data-ttu-id="26a59-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="26a59-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="26a59-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="26a59-117">See Also</span></span>

- [<span data-ttu-id="26a59-118">Micro soft. Quantum. Canon. ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="26a59-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="26a59-119">Micro soft. Quantum. Canon. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="26a59-119">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="26a59-120">Micro soft. Quantum. Canon. ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="26a59-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)