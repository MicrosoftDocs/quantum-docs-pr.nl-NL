---
uid: Microsoft.Quantum.Canon.RepeatCA
title: Bewerking RepeatCA
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: b68c3aa4298fffa76f7c43ac4c6d27cdf3b72fbf
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703857"
---
# <a name="repeatca-operation"></a><span data-ttu-id="11cef-102">Bewerking RepeatCA</span><span class="sxs-lookup"><span data-stu-id="11cef-102">RepeatCA operation</span></span>

<span data-ttu-id="11cef-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="11cef-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="11cef-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="11cef-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="11cef-105">Herhaalt een bewerking een bepaald aantal keren.</span><span class="sxs-lookup"><span data-stu-id="11cef-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatCA<'TInput> (op : ('TInput => Unit is Adj + Ctl), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="11cef-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="11cef-106">Input</span></span>

### <a name="op--tinput--unit-adj--ctl"></a><span data-ttu-id="11cef-107">op: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="11cef-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj + Ctl</span></span>

<span data-ttu-id="11cef-108">De bewerking die herhaaldelijk moet worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="11cef-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="11cef-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="11cef-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="11cef-110">Het aantal keren dat moet worden aangeroepen `op` .</span><span class="sxs-lookup"><span data-stu-id="11cef-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="11cef-111">invoer: ' TInput</span><span class="sxs-lookup"><span data-stu-id="11cef-111">input : 'TInput</span></span>

<span data-ttu-id="11cef-112">De invoer die moet worden door gegeven aan `op` .</span><span class="sxs-lookup"><span data-stu-id="11cef-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="11cef-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="11cef-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="11cef-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="11cef-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="11cef-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="11cef-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="11cef-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="11cef-116">See Also</span></span>

- [<span data-ttu-id="11cef-117">Micro soft. Quantum. arrays. DrawMany</span><span class="sxs-lookup"><span data-stu-id="11cef-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="11cef-118">Micro soft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="11cef-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="11cef-119">Micro soft. Quantum. Canon. Repeata</span><span class="sxs-lookup"><span data-stu-id="11cef-119">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="11cef-120">Micro soft. Quantum. Canon. RepeatC</span><span class="sxs-lookup"><span data-stu-id="11cef-120">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)