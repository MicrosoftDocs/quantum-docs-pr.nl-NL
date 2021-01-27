---
uid: Microsoft.Quantum.Arrays.DrawMany
title: Bewerking DrawMany
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: DrawMany
qsharp.summary: Repeats an operation for a given number of samples, collecting its outputs in an array.
ms.openlocfilehash: bf63ce308679cef97c776d3383ff732ed4d4e500
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846206"
---
# <a name="drawmany-operation"></a><span data-ttu-id="237c4-102">Bewerking DrawMany</span><span class="sxs-lookup"><span data-stu-id="237c4-102">DrawMany operation</span></span>

<span data-ttu-id="237c4-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="237c4-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="237c4-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="237c4-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="237c4-105">Hiermee wordt een bewerking herhaald voor een bepaald aantal steek proeven, waarbij de uitvoer ervan in een matrix wordt verzameld.</span><span class="sxs-lookup"><span data-stu-id="237c4-105">Repeats an operation for a given number of samples, collecting its outputs in an array.</span></span>

```qsharp
operation DrawMany<'TInput, 'TOutput> (op : ('TInput => 'TOutput), nSamples : Int, input : 'TInput) : 'TOutput[]
```


## <a name="input"></a><span data-ttu-id="237c4-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="237c4-106">Input</span></span>

### <a name="op--tinput--toutput"></a><span data-ttu-id="237c4-107">op: ' TInput => ' TOutput</span><span class="sxs-lookup"><span data-stu-id="237c4-107">op : 'TInput => 'TOutput</span></span> 

<span data-ttu-id="237c4-108">De bewerking die herhaaldelijk moet worden aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="237c4-108">The operation to be called repeatedly.</span></span>


### <a name="nsamples--int"></a><span data-ttu-id="237c4-109">nSamples: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="237c4-109">nSamples : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="237c4-110">Het aantal voor beelden van aanroepen `op` om te verzamelen.</span><span class="sxs-lookup"><span data-stu-id="237c4-110">The number of samples of calling `op` to collect.</span></span>


### <a name="input--tinput"></a><span data-ttu-id="237c4-111">invoer: ' TInput</span><span class="sxs-lookup"><span data-stu-id="237c4-111">input : 'TInput</span></span>

<span data-ttu-id="237c4-112">De invoer die moet worden door gegeven aan `op` .</span><span class="sxs-lookup"><span data-stu-id="237c4-112">The input to be passed to `op`.</span></span>



## <a name="output--toutput"></a><span data-ttu-id="237c4-113">Uitvoer: ' TOutput []</span><span class="sxs-lookup"><span data-stu-id="237c4-113">Output : 'TOutput[]</span></span>



## <a name="type-parameters"></a><span data-ttu-id="237c4-114">Type parameters</span><span class="sxs-lookup"><span data-stu-id="237c4-114">Type Parameters</span></span>

### <a name="tinput"></a><span data-ttu-id="237c4-115">'TInput</span><span class="sxs-lookup"><span data-stu-id="237c4-115">'TInput</span></span>


### <a name="toutput"></a><span data-ttu-id="237c4-116">'TOutput</span><span class="sxs-lookup"><span data-stu-id="237c4-116">'TOutput</span></span>



## <a name="example"></a><span data-ttu-id="237c4-117">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="237c4-117">Example</span></span>

<span data-ttu-id="237c4-118">De volgende steek proeven worden uitgevoerd op een geheel getal, op voor waarde dat een bewerking wordt uitgevoerd met één bit per keer.</span><span class="sxs-lookup"><span data-stu-id="237c4-118">The following samples an integer, given an operation that samples a single bit at a time.</span></span>

```qsharp
let randomInteger = BoolArrayAsInt(DrawMany(SampleRandomBit, 16, ()));
```

## <a name="see-also"></a><span data-ttu-id="237c4-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="237c4-119">See Also</span></span>

- [<span data-ttu-id="237c4-120">Micro soft. Quantum. Canon. Repeat</span><span class="sxs-lookup"><span data-stu-id="237c4-120">Microsoft.Quantum.Canon.Repeat</span></span>](xref:Microsoft.Quantum.Canon.Repeat)