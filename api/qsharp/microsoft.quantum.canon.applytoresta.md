---
uid: Microsoft.Quantum.Canon.ApplyToRestA
title: Bewerking ApplyToRestA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToRestA
qsharp.summary: Applies an operation to all but the first element of an array.
ms.openlocfilehash: 99a18e835115491cc3451a4e3b44a6ff70e9dc6c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704692"
---
# <a name="applytoresta-operation"></a><span data-ttu-id="a490e-102">Bewerking ApplyToRestA</span><span class="sxs-lookup"><span data-stu-id="a490e-102">ApplyToRestA operation</span></span>

<span data-ttu-id="a490e-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a490e-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a490e-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a490e-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a490e-105">Hiermee wordt een bewerking toegepast op alle, behalve het eerste element van een matrix.</span><span class="sxs-lookup"><span data-stu-id="a490e-105">Applies an operation to all but the first element of an array.</span></span>

```qsharp
operation ApplyToRestA<'T> (op : ('T[] => Unit is Adj), targets : 'T[]) : Unit
```


## <a name="description"></a><span data-ttu-id="a490e-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a490e-106">Description</span></span>

<span data-ttu-id="a490e-107">Als er een bewerking `op` en een matrix met doelen `targets` worden opgegeven, geldt `op(Rest(targets))` .</span><span class="sxs-lookup"><span data-stu-id="a490e-107">Given an operation `op` and an array of targets `targets`, applies `op(Rest(targets))`.</span></span>

## <a name="input"></a><span data-ttu-id="a490e-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="a490e-108">Input</span></span>

### <a name="op--t--unit-adj"></a><span data-ttu-id="a490e-109">op: 'T [] => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="a490e-109">op : 'T[] => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="a490e-110">Een bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="a490e-110">An operation to be applied.</span></span>


### <a name="targets--t"></a><span data-ttu-id="a490e-111">doelen: ' []</span><span class="sxs-lookup"><span data-stu-id="a490e-111">targets : 'T[]</span></span>

<span data-ttu-id="a490e-112">Een matrix met doelen, waarvan alles behalve de eerste wordt toegepast `op` .</span><span class="sxs-lookup"><span data-stu-id="a490e-112">An array of targets, of which all but the first will be applied to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a490e-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a490e-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a490e-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a490e-114">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a490e-115">T</span><span class="sxs-lookup"><span data-stu-id="a490e-115">'T</span></span>

<span data-ttu-id="a490e-116">Het invoer type van de bewerking die moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="a490e-116">The input type of the operation to be applied.</span></span>

## <a name="see-also"></a><span data-ttu-id="a490e-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a490e-117">See Also</span></span>

- [<span data-ttu-id="a490e-118">Micro soft. Quantum. Canon. ApplyToRest</span><span class="sxs-lookup"><span data-stu-id="a490e-118">Microsoft.Quantum.Canon.ApplyToRest</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRest)
- [<span data-ttu-id="a490e-119">Micro soft. Quantum. Canon. ApplyToRestC</span><span class="sxs-lookup"><span data-stu-id="a490e-119">Microsoft.Quantum.Canon.ApplyToRestC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestC)
- [<span data-ttu-id="a490e-120">Micro soft. Quantum. Canon. ApplyToRestCA</span><span class="sxs-lookup"><span data-stu-id="a490e-120">Microsoft.Quantum.Canon.ApplyToRestCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToRestCA)