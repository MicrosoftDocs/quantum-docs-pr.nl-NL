---
uid: Microsoft.Quantum.Canon.RepeatC
title: Bewerking RepeatC
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatC
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 8dc178374bdc9f8bf9f8aed57b9ae9a56995dec6
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703862"
---
# <a name="repeatc-operation"></a><span data-ttu-id="9a2b4-102">Bewerking RepeatC</span><span class="sxs-lookup"><span data-stu-id="9a2b4-102">RepeatC operation</span></span>

<span data-ttu-id="9a2b4-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9a2b4-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9a2b4-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9a2b4-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9a2b4-105">Herhaalt een bewerking een bepaald aantal keren.</span><span class="sxs-lookup"><span data-stu-id="9a2b4-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatC<'TInput> (op : ('TInput => Unit is Ctl), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="9a2b4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9a2b4-106">Input</span></span>

### <a name="op--tinput--unit-ctl"></a><span data-ttu-id="9a2b4-107">op: ' TInput = CTL van>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9a2b4-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) Ctl</span></span>

<span data-ttu-id="9a2b4-108">De bewerking die herhaaldelijk moet worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="9a2b4-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="9a2b4-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9a2b4-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9a2b4-110">Het aantal keren dat moet worden aangeroepen `op` .</span><span class="sxs-lookup"><span data-stu-id="9a2b4-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="9a2b4-111">invoer: ' TInput</span><span class="sxs-lookup"><span data-stu-id="9a2b4-111">input : 'TInput</span></span>

<span data-ttu-id="9a2b4-112">De invoer die moet worden door gegeven aan `op` .</span><span class="sxs-lookup"><span data-stu-id="9a2b4-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9a2b4-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9a2b4-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9a2b4-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9a2b4-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="9a2b4-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="9a2b4-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="9a2b4-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9a2b4-116">See Also</span></span>

- [<span data-ttu-id="9a2b4-117">Micro soft. Quantum. arrays. DrawMany</span><span class="sxs-lookup"><span data-stu-id="9a2b4-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="9a2b4-118">Micro soft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="9a2b4-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="9a2b4-119">Micro soft. Quantum. Canon. Repeata</span><span class="sxs-lookup"><span data-stu-id="9a2b4-119">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="9a2b4-120">Micro soft. Quantum. Canon. RepeatCA</span><span class="sxs-lookup"><span data-stu-id="9a2b4-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)