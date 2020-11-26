---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: De functie ConstantArray
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: 8cba68af2f1e178a1ef96921283f85e4feb498ea
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96210060"
---
# <a name="constantarray-function"></a><span data-ttu-id="f6efe-102">De functie ConstantArray</span><span class="sxs-lookup"><span data-stu-id="f6efe-102">ConstantArray function</span></span>

<span data-ttu-id="f6efe-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f6efe-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f6efe-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f6efe-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f6efe-105">Maakt een matrix met de opgegeven lengte en alle elementen die gelijk zijn aan de opgegeven waarde.</span><span class="sxs-lookup"><span data-stu-id="f6efe-105">Creates an array of given length with all elements equal to given value.</span></span>

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a><span data-ttu-id="f6efe-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="f6efe-106">Input</span></span>

### <a name="length--int"></a><span data-ttu-id="f6efe-107">lengte: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f6efe-107">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f6efe-108">Lengte van de nieuwe matrix.</span><span class="sxs-lookup"><span data-stu-id="f6efe-108">Length of the new array.</span></span>


### <a name="value--t"></a><span data-ttu-id="f6efe-109">waarde: 'T</span><span class="sxs-lookup"><span data-stu-id="f6efe-109">value : 'T</span></span>

<span data-ttu-id="f6efe-110">De waarde van elk element van de nieuwe matrix.</span><span class="sxs-lookup"><span data-stu-id="f6efe-110">The value of each element of the new array.</span></span>



## <a name="output--t"></a><span data-ttu-id="f6efe-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="f6efe-111">Output : 'T[]</span></span>

<span data-ttu-id="f6efe-112">Een nieuwe matrix met lengte `length` , zodat elk element is `value` .</span><span class="sxs-lookup"><span data-stu-id="f6efe-112">A new array of length `length`, such that every element is `value`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="f6efe-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="f6efe-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="f6efe-114">T</span><span class="sxs-lookup"><span data-stu-id="f6efe-114">'T</span></span>

