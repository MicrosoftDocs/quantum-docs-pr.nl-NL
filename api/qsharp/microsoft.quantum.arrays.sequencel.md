---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Sequence-functie
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 3e5c7f64825f09d82792d3e46fe3f53f5814510b
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220260"
---
# <a name="sequencel-function"></a><span data-ttu-id="107ab-102">Sequence-functie</span><span class="sxs-lookup"><span data-stu-id="107ab-102">SequenceL function</span></span>

<span data-ttu-id="107ab-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="107ab-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="107ab-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="107ab-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="107ab-105">Een matrix van gehele getallen ophalen binnen een bepaalde interval.</span><span class="sxs-lookup"><span data-stu-id="107ab-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceL (from : BigInt, to : BigInt) : BigInt[]
```


## <a name="input"></a><span data-ttu-id="107ab-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="107ab-106">Input</span></span>

### <a name="from--bigint"></a><span data-ttu-id="107ab-107">van: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="107ab-107">from : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="107ab-108">Een inclusieve start index van het interval.</span><span class="sxs-lookup"><span data-stu-id="107ab-108">An inclusive start index of the interval.</span></span>


### <a name="to--bigint"></a><span data-ttu-id="107ab-109">naar: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="107ab-109">to : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="107ab-110">Een inclusieve eind index van het interval dat niet kleiner is dan `from` .</span><span class="sxs-lookup"><span data-stu-id="107ab-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="107ab-111">Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]</span><span class="sxs-lookup"><span data-stu-id="107ab-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]</span></span>

<span data-ttu-id="107ab-112">Een matrix met de volg orde van getallen `from` , `from + 1` ,..., `to` .</span><span class="sxs-lookup"><span data-stu-id="107ab-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>

## <a name="remarks"></a><span data-ttu-id="107ab-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="107ab-113">Remarks</span></span>

<span data-ttu-id="107ab-114">Het verschil tussen `from` en `to` moet in een `Int` waarde passen.</span><span class="sxs-lookup"><span data-stu-id="107ab-114">The difference between `from` and `to` must fit into an `Int` value.</span></span>