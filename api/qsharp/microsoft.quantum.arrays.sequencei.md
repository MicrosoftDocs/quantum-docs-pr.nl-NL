---
uid: Microsoft.Quantum.Arrays.SequenceI
title: De functie SequenceI
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceI
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 5f03e5f2baff8077c1fa3fb5f1f079528ef0e215
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220294"
---
# <a name="sequencei-function"></a><span data-ttu-id="3cfdb-102">De functie SequenceI</span><span class="sxs-lookup"><span data-stu-id="3cfdb-102">SequenceI function</span></span>

<span data-ttu-id="3cfdb-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="3cfdb-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="3cfdb-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="3cfdb-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="3cfdb-105">Een matrix van gehele getallen ophalen binnen een bepaalde interval.</span><span class="sxs-lookup"><span data-stu-id="3cfdb-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceI (from : Int, to : Int) : Int[]
```


## <a name="input"></a><span data-ttu-id="3cfdb-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="3cfdb-106">Input</span></span>

### <a name="from--int"></a><span data-ttu-id="3cfdb-107">van: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3cfdb-107">from : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3cfdb-108">Een inclusieve start index van het interval.</span><span class="sxs-lookup"><span data-stu-id="3cfdb-108">An inclusive start index of the interval.</span></span>


### <a name="to--int"></a><span data-ttu-id="3cfdb-109">naar: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="3cfdb-109">to : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="3cfdb-110">Een inclusieve eind index van het interval dat niet kleiner is dan `from` .</span><span class="sxs-lookup"><span data-stu-id="3cfdb-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--int"></a><span data-ttu-id="3cfdb-111">Output: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="3cfdb-111">Output : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="3cfdb-112">Een matrix met de volg orde van getallen `from` , `from + 1` ,..., `to` .</span><span class="sxs-lookup"><span data-stu-id="3cfdb-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>