---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Bewerking AllowAtMostNCallsCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: 7caf33e33318bb74cb160436940eff9f0f2782cc
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202563"
---
# <a name="allowatmostncallsca-operation"></a><span data-ttu-id="c2267-102">Bewerking AllowAtMostNCallsCA</span><span class="sxs-lookup"><span data-stu-id="c2267-102">AllowAtMostNCallsCA operation</span></span>

<span data-ttu-id="c2267-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="c2267-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="c2267-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="c2267-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="c2267-105">Tussen een aanroep van deze bewerking en de adjoint wordt bevestigd dat een bepaalde bewerking Maxi maal een bepaald aantal keer wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="c2267-105">Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.</span></span>

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="c2267-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c2267-106">Input</span></span>

### <a name="ntimes--int"></a><span data-ttu-id="c2267-107">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c2267-107">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c2267-108">Het maximum aantal keer dat `op` kan worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="c2267-108">The maximum number of times that `op` may be called.</span></span>


### <a name="op--tinput--toutput--is-adj--ctl"></a><span data-ttu-id="c2267-109">op: ' TInput => ' TOutput is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="c2267-109">op : 'TInput => 'TOutput  is Adj + Ctl</span></span>

<span data-ttu-id="c2267-110">Een bewerking waarvan de aanroepen moeten worden beperkt.</span><span class="sxs-lookup"><span data-stu-id="c2267-110">An operation whose calls are to be restricted.</span></span>


### <a name="message--string"></a><span data-ttu-id="c2267-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="c2267-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="c2267-112">Een bericht dat wordt weer gegeven wanneer de fout is opgetreden.</span><span class="sxs-lookup"><span data-stu-id="c2267-112">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c2267-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c2267-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c2267-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="c2267-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="c2267-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="c2267-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="c2267-116">'TOutput</span><span class="sxs-lookup"><span data-stu-id="c2267-116">'TOutput</span></span>



## <a name="remarks"></a><span data-ttu-id="c2267-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c2267-117">Remarks</span></span>

<span data-ttu-id="c2267-118">Deze bewerking kan worden vervangen door een van de doelen die deze niet ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="c2267-118">This operation may be replaced by a no-op on targets which do not support it.</span></span>