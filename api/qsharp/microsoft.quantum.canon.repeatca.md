---
uid: Microsoft.Quantum.Canon.RepeatCA
title: Bewerking RepeatCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatCA
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: af93220562d6be27b2f41e770bd953e5e808fcbf
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852214"
---
# <a name="repeatca-operation"></a><span data-ttu-id="fb0d2-102">Bewerking RepeatCA</span><span class="sxs-lookup"><span data-stu-id="fb0d2-102">RepeatCA operation</span></span>

<span data-ttu-id="fb0d2-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fb0d2-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fb0d2-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fb0d2-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fb0d2-105">Herhaalt een bewerking een bepaald aantal keren.</span><span class="sxs-lookup"><span data-stu-id="fb0d2-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatCA<'TInput> (op : ('TInput => Unit is Adj + Ctl), nTimes : Int, input : 'TInput) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="fb0d2-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="fb0d2-106">Input</span></span>

### <a name="op--tinput--unit--is-adj--ctl"></a><span data-ttu-id="fb0d2-107">op: ' TInput => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="fb0d2-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="fb0d2-108">De bewerking die herhaaldelijk moet worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="fb0d2-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="fb0d2-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="fb0d2-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="fb0d2-110">Het aantal keren dat moet worden aangeroepen `op` .</span><span class="sxs-lookup"><span data-stu-id="fb0d2-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="fb0d2-111">invoer: ' TInput</span><span class="sxs-lookup"><span data-stu-id="fb0d2-111">input : 'TInput</span></span>

<span data-ttu-id="fb0d2-112">De invoer die moet worden door gegeven aan `op` .</span><span class="sxs-lookup"><span data-stu-id="fb0d2-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fb0d2-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fb0d2-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="fb0d2-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="fb0d2-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="fb0d2-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="fb0d2-115">'TInput</span></span>



## <a name="example"></a><span data-ttu-id="fb0d2-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="fb0d2-116">Example</span></span>

<span data-ttu-id="fb0d2-117">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="fb0d2-117">The following are equivalent:</span></span>

```qsharp
RepeatCA(U, 17, target);
(BoundCA(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a><span data-ttu-id="fb0d2-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="fb0d2-118">See Also</span></span>

- [<span data-ttu-id="fb0d2-119">Micro soft. Quantum. arrays. DrawMany</span><span class="sxs-lookup"><span data-stu-id="fb0d2-119">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="fb0d2-120">Micro soft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="fb0d2-120">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="fb0d2-121">Micro soft. Quantum. Canon. Repeata</span><span class="sxs-lookup"><span data-stu-id="fb0d2-121">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="fb0d2-122">Micro soft. Quantum. Canon. RepeatC</span><span class="sxs-lookup"><span data-stu-id="fb0d2-122">Microsoft.Quantum.Canon.RepeatC</span></span>](xref:Microsoft.Quantum.Canon.RepeatC)