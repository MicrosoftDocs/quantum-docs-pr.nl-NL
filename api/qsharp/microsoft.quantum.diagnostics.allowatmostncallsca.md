---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNCallsCA
title: Bewerking AllowAtMostNCallsCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNCallsCA
qsharp.summary: Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.
ms.openlocfilehash: bb6ba2615b571b0d9d056b93f8e36d2dec0c4a21
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98853541"
---
# <a name="allowatmostncallsca-operation"></a><span data-ttu-id="9ed9b-102">Bewerking AllowAtMostNCallsCA</span><span class="sxs-lookup"><span data-stu-id="9ed9b-102">AllowAtMostNCallsCA operation</span></span>

<span data-ttu-id="9ed9b-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="9ed9b-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="9ed9b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9ed9b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9ed9b-105">Tussen een aanroep van deze bewerking en de adjoint wordt bevestigd dat een bepaalde bewerking Maxi maal een bepaald aantal keer wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-105">Between a call to this operation and its adjoint, asserts that a given operation is called at most a certain number of times.</span></span>

```qsharp
operation AllowAtMostNCallsCA<'TInput, 'TOutput> (nTimes : Int, op : ('TInput => 'TOutput is Adj + Ctl), message : String) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="9ed9b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9ed9b-106">Input</span></span>

### <a name="ntimes--int"></a><span data-ttu-id="9ed9b-107">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9ed9b-107">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9ed9b-108">Het maximum aantal keer dat `op` kan worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-108">The maximum number of times that `op` may be called.</span></span>


### <a name="op--tinput--toutput--is-adj--ctl"></a><span data-ttu-id="9ed9b-109">op: ' TInput => ' TOutput is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="9ed9b-109">op : 'TInput => 'TOutput  is Adj + Ctl</span></span>

<span data-ttu-id="9ed9b-110">Een bewerking waarvan de aanroepen moeten worden beperkt.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-110">An operation whose calls are to be restricted.</span></span>


### <a name="message--string"></a><span data-ttu-id="9ed9b-111">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="9ed9b-111">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="9ed9b-112">Een bericht dat wordt weer gegeven wanneer de fout is opgetreden.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-112">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9ed9b-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9ed9b-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9ed9b-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9ed9b-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="9ed9b-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="9ed9b-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="9ed9b-116">'TOutput</span><span class="sxs-lookup"><span data-stu-id="9ed9b-116">'TOutput</span></span>



## <a name="example"></a><span data-ttu-id="9ed9b-117">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="9ed9b-117">Example</span></span>

<span data-ttu-id="9ed9b-118">Het volgende code fragment mislukt wanneer dit wordt uitgevoerd op machines die deze diagnose ondersteunen:</span><span class="sxs-lookup"><span data-stu-id="9ed9b-118">The following snippet will fail when executed on machines which support this diagnostic:</span></span>

```qsharp
using (register = Qubit[4]) {
    within {
        AllowAtMostNCallsCA(3, H, "Too many calls to H.");
    } apply {
        // Fails since this calls H four times, rather than the
        // allowed maximum of three.
        ApplyToEach(H, register);
    }
}
```

## <a name="remarks"></a><span data-ttu-id="9ed9b-119">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="9ed9b-119">Remarks</span></span>

<span data-ttu-id="9ed9b-120">Deze bewerking kan worden vervangen door een van de doelen die deze niet ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="9ed9b-120">This operation may be replaced by a no-op on targets which do not support it.</span></span>