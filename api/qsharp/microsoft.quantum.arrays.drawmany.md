---
uid: Microsoft.Quantum.Arrays.DrawMany
title: Bewerking DrawMany
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: 601fe603a869dcf977c1ceade5819ee64f634d53
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706109"
---
# <a name="drawmany-operation"></a><span data-ttu-id="a44da-102">Bewerking DrawMany</span><span class="sxs-lookup"><span data-stu-id="a44da-102">DrawMany operation</span></span>

<span data-ttu-id="a44da-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a44da-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a44da-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="a44da-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="a44da-105">Hiermee wordt een bewerking herhaald voor een bepaald aantal steek proeven, waarbij de uitvoer ervan in een matrix wordt verzameld.</span><span class="sxs-lookup"><span data-stu-id="a44da-105">Repeats an operation for a given number of samples, collecting its outputs in an array.</span></span>

```qsharp
operation DrawMany<'TInput, 'TOutput> (op : ('TInput => 'TOutput), nSamples : Int, input : 'TInput) : 'TOutput[]
```


## <a name="input"></a><span data-ttu-id="a44da-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a44da-106">Input</span></span>

### <a name="op--tinput--toutput"></a><span data-ttu-id="a44da-107">op: ' TInput => ' TOutput</span><span class="sxs-lookup"><span data-stu-id="a44da-107">op : 'TInput => 'TOutput</span></span> 

<span data-ttu-id="a44da-108">De bewerking die herhaaldelijk moet worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="a44da-108">The operation to be called repeatedly.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="a44da-109">nSamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="a44da-109">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="a44da-110">Het aantal voor beelden van aanroepen `op` om te verzamelen.</span><span class="sxs-lookup"><span data-stu-id="a44da-110">The number of samples of calling `op` to collect.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="a44da-111">invoer: ' TInput</span><span class="sxs-lookup"><span data-stu-id="a44da-111">input : 'TInput</span></span>

<span data-ttu-id="a44da-112">De invoer die moet worden door gegeven aan `op` .</span><span class="sxs-lookup"><span data-stu-id="a44da-112">The input to be passed to `op`.</span></span>



## <a name="output--toutput"></a><span data-ttu-id="a44da-113">Uitvoer: ' TOutput []</span><span class="sxs-lookup"><span data-stu-id="a44da-113">Output : 'TOutput[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="a44da-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a44da-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="a44da-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="a44da-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="a44da-116">'TOutput</span><span class="sxs-lookup"><span data-stu-id="a44da-116">'TOutput</span></span>



## <a name="see-also"></a><span data-ttu-id="a44da-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a44da-117">See Also</span></span>

- [<span data-ttu-id="a44da-118">Micro soft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="a44da-118">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)