---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Sequence-functie
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: d5ce63575e703341fce42c0be393765c342bbd89
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705781"
---
# <a name="sequencel-function"></a><span data-ttu-id="faa56-102">Sequence-functie</span><span class="sxs-lookup"><span data-stu-id="faa56-102">SequenceL function</span></span>

<span data-ttu-id="faa56-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="faa56-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="faa56-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="faa56-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="faa56-105">Een matrix van gehele getallen ophalen binnen een bepaalde interval.</span><span class="sxs-lookup"><span data-stu-id="faa56-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceL (from : BigInt, to : BigInt) : BigInt[]
```


## <a name="input"></a><span data-ttu-id="faa56-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="faa56-106">Input</span></span>

### <a name="from--bigint"></a><span data-ttu-id="faa56-107">van: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="faa56-107">from : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="faa56-108">Een inclusieve start index van het interval.</span><span class="sxs-lookup"><span data-stu-id="faa56-108">An inclusive start index of the interval.</span></span>


### <a name="to--bigint"></a><span data-ttu-id="faa56-109">naar: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="faa56-109">to : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="faa56-110">Een inclusieve eind index van het interval dat niet kleiner is dan `from` .</span><span class="sxs-lookup"><span data-stu-id="faa56-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="faa56-111">Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]</span><span class="sxs-lookup"><span data-stu-id="faa56-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]</span></span>

<span data-ttu-id="faa56-112">Een matrix met de volg orde van getallen `from` , `from + 1` ,..., `to` .</span><span class="sxs-lookup"><span data-stu-id="faa56-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>

## <a name="remarks"></a><span data-ttu-id="faa56-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="faa56-113">Remarks</span></span>

<span data-ttu-id="faa56-114">Het verschil tussen `from` en `to` moet in een `Int` waarde passen.</span><span class="sxs-lookup"><span data-stu-id="faa56-114">The difference between `from` and `to` must fit into an `Int` value.</span></span>