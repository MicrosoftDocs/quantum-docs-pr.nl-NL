---
uid: Microsoft.Quantum.Canon.Repeat
title: Bewerking herhalen
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: Repeat
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: 5aedd056b851b8d8d7c25a32eb22587292e132a8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92703880"
---
# <a name="repeat-operation"></a><span data-ttu-id="c07d7-102">Bewerking herhalen</span><span class="sxs-lookup"><span data-stu-id="c07d7-102">Repeat operation</span></span>

<span data-ttu-id="c07d7-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="c07d7-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="c07d7-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c07d7-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c07d7-105">Herhaalt een bewerking een bepaald aantal keren.</span><span class="sxs-lookup"><span data-stu-id="c07d7-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation Repeat<'TInput> (op : ('TInput => Unit), nTimes : Int, input : 'TInput) : Unit
```


## <a name="input"></a><span data-ttu-id="c07d7-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c07d7-106">Input</span></span>

### <a name="op--tinput--unit"></a><span data-ttu-id="c07d7-107">op: ' TInput =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c07d7-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="c07d7-108">De bewerking die herhaaldelijk moet worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="c07d7-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="c07d7-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c07d7-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c07d7-110">Het aantal keren dat moet worden aangeroepen `op` .</span><span class="sxs-lookup"><span data-stu-id="c07d7-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="c07d7-111">invoer: ' TInput</span><span class="sxs-lookup"><span data-stu-id="c07d7-111">input : 'TInput</span></span>

<span data-ttu-id="c07d7-112">De invoer die moet worden door gegeven aan `op` .</span><span class="sxs-lookup"><span data-stu-id="c07d7-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c07d7-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c07d7-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="c07d7-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="c07d7-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="c07d7-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="c07d7-115">'TInput</span></span>



## <a name="see-also"></a><span data-ttu-id="c07d7-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c07d7-116">See Also</span></span>

- [<span data-ttu-id="c07d7-117">Micro soft. Quantum. arrays. DrawMany</span><span class="sxs-lookup"><span data-stu-id="c07d7-117">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="c07d7-118">Micro soft. Quantum. Canon. Repeata</span><span class="sxs-lookup"><span data-stu-id="c07d7-118">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="c07d7-119">Micro soft. Quantum. Canon. RepeatC</span><span class="sxs-lookup"><span data-stu-id="c07d7-119">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)
- [<span data-ttu-id="c07d7-120">Micro soft. Quantum. Canon. RepeatCA</span><span class="sxs-lookup"><span data-stu-id="c07d7-120">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)