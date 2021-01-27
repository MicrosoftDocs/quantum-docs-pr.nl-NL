---
uid: Microsoft.Quantum.Arrays.SequenceL
title: Sequence-functie
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: SequenceL
qsharp.summary: Get an array of integers in a given interval.
ms.openlocfilehash: 7e3c5c31428f9be152e28afbe478a3d15eb0a56c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850991"
---
# <a name="sequencel-function"></a><span data-ttu-id="7016f-102">Sequence-functie</span><span class="sxs-lookup"><span data-stu-id="7016f-102">SequenceL function</span></span>

<span data-ttu-id="7016f-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="7016f-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="7016f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="7016f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="7016f-105">Een matrix van gehele getallen ophalen binnen een bepaalde interval.</span><span class="sxs-lookup"><span data-stu-id="7016f-105">Get an array of integers in a given interval.</span></span>

```qsharp
function SequenceL (from : BigInt, to : BigInt) : BigInt[]
```


## <a name="input"></a><span data-ttu-id="7016f-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="7016f-106">Input</span></span>

### <a name="from--bigint"></a><span data-ttu-id="7016f-107">van: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="7016f-107">from : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="7016f-108">Een inclusieve start index van het interval.</span><span class="sxs-lookup"><span data-stu-id="7016f-108">An inclusive start index of the interval.</span></span>


### <a name="to--bigint"></a><span data-ttu-id="7016f-109">naar: [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span><span class="sxs-lookup"><span data-stu-id="7016f-109">to : [BigInt](xref:microsoft.quantum.lang-ref.bigint)</span></span>

<span data-ttu-id="7016f-110">Een inclusieve eind index van het interval dat niet kleiner is dan `from` .</span><span class="sxs-lookup"><span data-stu-id="7016f-110">An inclusive end index of the interval that is not smaller than `from`.</span></span>



## <a name="output--bigint"></a><span data-ttu-id="7016f-111">Uitvoer: [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]</span><span class="sxs-lookup"><span data-stu-id="7016f-111">Output : [BigInt](xref:microsoft.quantum.lang-ref.bigint)[]</span></span>

<span data-ttu-id="7016f-112">Een matrix met de volg orde van getallen `from` , `from + 1` ,..., `to` .</span><span class="sxs-lookup"><span data-stu-id="7016f-112">An array containing the sequence of numbers `from`, `from + 1`, ..., `to`.</span></span>

## <a name="example"></a><span data-ttu-id="7016f-113">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="7016f-113">Example</span></span>

```qsharp
let arr1 = SequenceL(0L, 3L); // [0L, 1L, 2L, 3L]
let arr2 = SequenceL(23L, 29L); // [23L, 24L, 25L, 26L, 27L, 28L, 29L]
let arr3 = SequenceL(-5L, -2L); // [-5L, -4L, -3L, -2L]
```

## <a name="remarks"></a><span data-ttu-id="7016f-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="7016f-114">Remarks</span></span>

<span data-ttu-id="7016f-115">Het verschil tussen `from` en `to` moet in een `Int` waarde passen.</span><span class="sxs-lookup"><span data-stu-id="7016f-115">The difference between `from` and `to` must fit into an `Int` value.</span></span>