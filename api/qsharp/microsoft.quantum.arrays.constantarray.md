---
uid: Microsoft.Quantum.Arrays.ConstantArray
title: De functie ConstantArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: ConstantArray
qsharp.summary: Creates an array of given length with all elements equal to given value.
ms.openlocfilehash: 848f18944829d08a10ec602dcb5d99c100c81f76
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706140"
---
# <a name="constantarray-function"></a><span data-ttu-id="c1b52-102">De functie ConstantArray</span><span class="sxs-lookup"><span data-stu-id="c1b52-102">ConstantArray function</span></span>

<span data-ttu-id="c1b52-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c1b52-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c1b52-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c1b52-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c1b52-105">Maakt een matrix met de opgegeven lengte en alle elementen die gelijk zijn aan de opgegeven waarde.</span><span class="sxs-lookup"><span data-stu-id="c1b52-105">Creates an array of given length with all elements equal to given value.</span></span>

```qsharp
function ConstantArray<'T> (length : Int, value : 'T) : 'T[]
```


## <a name="input"></a><span data-ttu-id="c1b52-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="c1b52-106">Input</span></span>

### <a name="length--int"></a><span data-ttu-id="c1b52-107">lengte: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c1b52-107">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c1b52-108">Lengte van de nieuwe matrix.</span><span class="sxs-lookup"><span data-stu-id="c1b52-108">Length of the new array.</span></span>


### <a name="value--t"></a><span data-ttu-id="c1b52-109">waarde: 'T</span><span class="sxs-lookup"><span data-stu-id="c1b52-109">value : 'T</span></span>

<span data-ttu-id="c1b52-110">De waarde van elk element van de nieuwe matrix.</span><span class="sxs-lookup"><span data-stu-id="c1b52-110">The value of each element of the new array.</span></span>



## <a name="output--t"></a><span data-ttu-id="c1b52-111">Uitvoer: ' []</span><span class="sxs-lookup"><span data-stu-id="c1b52-111">Output : 'T[]</span></span>

<span data-ttu-id="c1b52-112">Een nieuwe matrix met lengte `length` , zodat elk element is `value` .</span><span class="sxs-lookup"><span data-stu-id="c1b52-112">A new array of length `length`, such that every element is `value`.</span></span>

## <a name="type-parameters"></a><span data-ttu-id="c1b52-113">Type parameters</span><span class="sxs-lookup"><span data-stu-id="c1b52-113">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="c1b52-114">T</span><span class="sxs-lookup"><span data-stu-id="c1b52-114">'T</span></span>

