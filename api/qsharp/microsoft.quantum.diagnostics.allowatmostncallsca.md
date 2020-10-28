---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Bewerking AllowAtMostNCallsCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: 1a9975d2d2026749238430b247cf47738de545cd
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702794"
---
# <a name="allowatmostncallsca-operation"></a><span data-ttu-id="a1aee-102">Bewerking AllowAtMostNCallsCA</span><span class="sxs-lookup"><span data-stu-id="a1aee-102">AllowAtMostNCallsCA operation</span></span>

<span data-ttu-id="a1aee-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="a1aee-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="a1aee-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a1aee-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a1aee-105">Tussen een aanroep van deze bewerking en de adjoint wordt bevestigd dat een bepaalde bewerking Maxi maal een bepaald aantal keer wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="a1aee-105">Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.</span></span>

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="a1aee-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a1aee-106">Input</span></span>

### <a name="ntimes--int"></a><span data-ttu-id="a1aee-107">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a1aee-107">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a1aee-108">Het maximum aantal keer dat `op` kan worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="a1aee-108">The maximum number of times that `op` may be called.</span></span>


### <a name="op--tinput--toutput-adj--ctl"></a><span data-ttu-id="a1aee-109">op: ' TInput => ' TOutput ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="a1aee-109">op : 'TInput => 'TOutput Adj + Ctl</span></span>

<span data-ttu-id="a1aee-110">Een bewerking waarvan de aanroepen moeten worden beperkt.</span><span class="sxs-lookup"><span data-stu-id="a1aee-110">An operation whose calls are to be restricted.</span></span>


### <a name="message--string"></a><span data-ttu-id="a1aee-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="a1aee-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="a1aee-112">Een bericht dat wordt weer gegeven wanneer de fout is opgetreden.</span><span class="sxs-lookup"><span data-stu-id="a1aee-112">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a1aee-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a1aee-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a1aee-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a1aee-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="a1aee-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="a1aee-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="a1aee-116">'TOutput</span><span class="sxs-lookup"><span data-stu-id="a1aee-116">'TOutput</span></span>



## <a name="remarks"></a><span data-ttu-id="a1aee-117">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="a1aee-117">Remarks</span></span>

<span data-ttu-id="a1aee-118">Deze bewerking kan worden vervangen door een van de doelen die deze niet ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="a1aee-118">This operation may be replaced by a no-op on targets which do not support it.</span></span>