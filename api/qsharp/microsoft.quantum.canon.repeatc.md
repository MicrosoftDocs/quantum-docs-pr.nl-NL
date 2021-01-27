---
uid: Microsoft.Quantum.Canon.RepeatC
title: Bewerking RepeatC
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: RepeatC
qsharp.summary: Repeats an operation a given number of times.
ms.openlocfilehash: efb820411be63352fc09ada2441a9140dd5575f9
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840240"
---
# <a name="repeatc-operation"></a><span data-ttu-id="9d51b-102">Bewerking RepeatC</span><span class="sxs-lookup"><span data-stu-id="9d51b-102">RepeatC operation</span></span>

<span data-ttu-id="9d51b-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9d51b-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9d51b-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9d51b-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9d51b-105">Herhaalt een bewerking een bepaald aantal keren.</span><span class="sxs-lookup"><span data-stu-id="9d51b-105">Repeats an operation a given number of times.</span></span>

```qsharp
operation RepeatC<'TInput> (op : ('TInput => Unit is Ctl), nTimes : Int, input : 'TInput) : Unit is Ctl
```


## <a name="input"></a><span data-ttu-id="9d51b-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="9d51b-106">Input</span></span>

### <a name="op--tinput--unit--is-ctl"></a><span data-ttu-id="9d51b-107">op: ' TInput =>- [eenheid](xref:microsoft.quantum.lang-ref.unit)  is CTL</span><span class="sxs-lookup"><span data-stu-id="9d51b-107">op : 'TInput => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Ctl</span></span>

<span data-ttu-id="9d51b-108">De bewerking die herhaaldelijk moet worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="9d51b-108">The operation to be called repeatedly.</span></span>


### <a name="ntimes--int"></a><span data-ttu-id="9d51b-109">nTimes: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="9d51b-109">nTimes : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="9d51b-110">Het aantal keren dat moet worden aangeroepen `op` .</span><span class="sxs-lookup"><span data-stu-id="9d51b-110">The number of times to call `op`.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="9d51b-111">invoer: ' TInput</span><span class="sxs-lookup"><span data-stu-id="9d51b-111">input : 'TInput</span></span>

<span data-ttu-id="9d51b-112">De invoer die moet worden door gegeven aan `op` .</span><span class="sxs-lookup"><span data-stu-id="9d51b-112">The input to be passed to `op`.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9d51b-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9d51b-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="type-parameters"></a><span data-ttu-id="9d51b-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="9d51b-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="9d51b-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="9d51b-115">'TInput</span></span>



## <a name="example"></a><span data-ttu-id="9d51b-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="9d51b-116">Example</span></span>

<span data-ttu-id="9d51b-117">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="9d51b-117">The following are equivalent:</span></span>

```qsharp
RepeatC(U, 17, target);
(BoundC(ConstantArray(17, U)))(target);
```

## <a name="see-also"></a><span data-ttu-id="9d51b-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="9d51b-118">See Also</span></span>

- [<span data-ttu-id="9d51b-119">Micro soft. Quantum. arrays. DrawMany</span><span class="sxs-lookup"><span data-stu-id="9d51b-119">Microsoft.Quantum.Arrays.DrawMany</span></span>](xref:Microsoft.Quantum.Arrays.DrawMany)
- [<span data-ttu-id="9d51b-120">Micro soft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="9d51b-120">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)
- [<span data-ttu-id="9d51b-121">Micro soft. Quantum. Canon. Repeata</span><span class="sxs-lookup"><span data-stu-id="9d51b-121">Microsoft.Quantum.Canon.RepeatA</span></span>](xref:Microsoft.Quantum.Canon.RepeatA)
- [<span data-ttu-id="9d51b-122">Micro soft. Quantum. Canon. RepeatCA</span><span class="sxs-lookup"><span data-stu-id="9d51b-122">Microsoft.Quantum.Canon.RepeatCA</span></span>](xref:Microsoft.Quantum.Canon.RepeatCA)