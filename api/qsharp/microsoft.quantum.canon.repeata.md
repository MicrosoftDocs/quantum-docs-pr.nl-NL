---
uid: Microsoft.Quantum.Canon.RepeatA
title: Herhaala-bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 5f418f67d7265d4cb39b3636906c74d33d80f472
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96205555"
---
# <a name="repeata-operation"></a><span data-ttu-id="09bfb-102">Herhaala-bewerking</span><span class="sxs-lookup"><span data-stu-id="09bfb-102">RepeatA operation</span></span>

<span data-ttu-id="09bfb-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="09bfb-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="09bfb-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="09bfb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="09bfb-105">Herhaalt een bewerking een bepaald aantal keren.</span><span class="sxs-lookup"><span data-stu-id="09bfb-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatA<'TInput> (op : ('TInput => Unit is Adj), nTimes : Int, input : 'TInput) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="09bfb-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="09bfb-106">Input</span></span>

### <a name="op--tinput--unit--is-adj"></a><span data-ttu-id="09bfb-107">op: ' TInput => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="09bfb-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="09bfb-108">De bewerking die herhaaldelijk moet worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="09bfb-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="09bfb-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="09bfb-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="09bfb-110">Het aantal keren dat moet worden aangeroepen `op` .</span><span class="sxs-lookup"><span data-stu-id="09bfb-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="09bfb-111">invoer: ' TInput</span><span class="sxs-lookup"><span data-stu-id="09bfb-111">input : 'TInput</span></span>

<span data-ttu-id="09bfb-112">De invoer die moet worden door gegeven aan `op` .</span><span class="sxs-lookup"><span data-stu-id="09bfb-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="09bfb-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="09bfb-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="09bfb-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="09bfb-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="09bfb-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="09bfb-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="09bfb-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="09bfb-116">See Also</span></span>

- [<span data-ttu-id="09bfb-117">Micro soft. Quantum. arrays. DrawMany</span><span class="sxs-lookup"><span data-stu-id="09bfb-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="09bfb-118">Micro soft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="09bfb-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="09bfb-119">Micro soft. Quantum. Canon. RepeatC</span><span class="sxs-lookup"><span data-stu-id="09bfb-119">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="09bfb-120">Micro soft. Quantum. Canon. RepeatCA</span><span class="sxs-lookup"><span data-stu-id="09bfb-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)