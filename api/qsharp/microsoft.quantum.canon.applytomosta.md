---
uid: Microsoft.Quantum.Canon.ApplyToMostA
title: Bewerking ApplyToMostA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToMostA
qsharp.summary: Applies an operation to all but the last element of an array.
ms.openlocfilehash: eb793b3d6bc1f75a14e97420d36d0aea3038e0f5
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850574"
---
# <a name="applytomosta-operation"></a><span data-ttu-id="6f890-102">Bewerking ApplyToMostA</span><span class="sxs-lookup"><span data-stu-id="6f890-102">ApplyToMostA operation</span></span>

<span data-ttu-id="6f890-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="6f890-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="6f890-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="6f890-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="6f890-105">Hiermee wordt een bewerking toegepast op alle, behalve het laatste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="6f890-105">Applies an operation to all but the last element of an array.</span></span>

```qsharp
operation ApplyToMostA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit is Adj
```


## <a name="description"></a><span data-ttu-id="6f890-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6f890-106">Description</span></span>

<span data-ttu-id="6f890-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Most(targets))` .</span><span class="sxs-lookup"><span data-stu-id="6f890-107">Given an operation `op` and an array of targets `targets`, applies `op(Most(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="6f890-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="6f890-108">Input</span></span>

### <a name="op--t--unit--is-adj"></a><span data-ttu-id="6f890-109">op: 'T [] => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="6f890-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="6f890-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="6f890-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="6f890-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="6f890-111">targets : 'T[]</span></span>

<span data-ttu-id="6f890-112">Een matrix met doelen, waarvan alles behalve de laatste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="6f890-112">An array of targets, of which all but the last will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="6f890-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="6f890-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="6f890-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="6f890-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="6f890-115">T</span><span class="sxs-lookup"><span data-stu-id="6f890-115">'T</span></span>

<span data-ttu-id="6f890-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="6f890-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="6f890-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6f890-117">See Also</span></span>

- [<span data-ttu-id="6f890-118">Micro soft. Quantum. Canon. ApplyToMost</span><span class="sxs-lookup"><span data-stu-id="6f890-118">Microsoft.Quantum.Canon.ApplyToMost</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMost)
- [<span data-ttu-id="6f890-119">Micro soft. Quantum. Canon. ApplyToMostC</span><span class="sxs-lookup"><span data-stu-id="6f890-119">Microsoft.Quantum.Canon.ApplyToMostC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostC)
- [<span data-ttu-id="6f890-120">Micro soft. Quantum. Canon. ApplyToMostCA</span><span class="sxs-lookup"><span data-stu-id="6f890-120">Microsoft.Quantum.Canon.ApplyToMostCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToMostCA)