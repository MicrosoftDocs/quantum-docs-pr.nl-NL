---
uid: Microsoft.Quantum.Canon.RepeatA
title: Herhaala-bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 89d34e5a30a61dee392904ce1076605432e21395
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703863"
---
# <a name="repeata-operation"></a><span data-ttu-id="e2c65-102">Herhaala-bewerking</span><span class="sxs-lookup"><span data-stu-id="e2c65-102">RepeatA operation</span></span>

<span data-ttu-id="e2c65-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="e2c65-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="e2c65-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e2c65-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e2c65-105">Herhaalt een bewerking een bepaald aantal keren.</span><span class="sxs-lookup"><span data-stu-id="e2c65-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatA<'TInput> (op : ('TInput => Unit is Adj), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="e2c65-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e2c65-106">Input</span></span>

### <a name="op--tinput--unit-adj"></a><span data-ttu-id="e2c65-107">op: ' TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) ADJ</span><span class="sxs-lookup"><span data-stu-id="e2c65-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit) Adj</span></span>

<span data-ttu-id="e2c65-108">De bewerking die herhaaldelijk moet worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="e2c65-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="e2c65-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e2c65-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e2c65-110">Het aantal keren dat moet worden aangeroepen `op` .</span><span class="sxs-lookup"><span data-stu-id="e2c65-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="e2c65-111">invoer: ' TInput</span><span class="sxs-lookup"><span data-stu-id="e2c65-111">input : 'TInput</span></span>

<span data-ttu-id="e2c65-112">De invoer die moet worden door gegeven aan `op` .</span><span class="sxs-lookup"><span data-stu-id="e2c65-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e2c65-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e2c65-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="e2c65-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="e2c65-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="e2c65-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="e2c65-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="e2c65-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="e2c65-116">See Also</span></span>

- [<span data-ttu-id="e2c65-117">Micro soft. Quantum. arrays. DrawMany</span><span class="sxs-lookup"><span data-stu-id="e2c65-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="e2c65-118">Micro soft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="e2c65-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="e2c65-119">Micro soft. Quantum. Canon. RepeatC</span><span class="sxs-lookup"><span data-stu-id="e2c65-119">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="e2c65-120">Micro soft. Quantum. Canon. RepeatCA</span><span class="sxs-lookup"><span data-stu-id="e2c65-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)