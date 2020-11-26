---
uid: Microsoft.Quantum.Diagnostics._iterateThroughCartesianPower
title: _iterateThroughCartesianPower bewerking
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: _iterateThroughCartesianPower
qsharp.summary: Iterates a variable through a Cartesian product [ 0, bounds[0]-1 ] × [ 0, bounds[1]-1 ] × [ 0, bounds[Length(bounds)-1]-1 ] and calls op(arr) for every element of the Cartesian product
ms.openlocfilehash: cde25eb99c9e1bde080c5356ecabd9f12cde9bba
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96213715"
---
# <a name="_iteratethroughcartesianpower-operation"></a><span data-ttu-id="e44a9-102">_iterateThroughCartesianPower bewerking</span><span class="sxs-lookup"><span data-stu-id="e44a9-102">_iterateThroughCartesianPower operation</span></span>

<span data-ttu-id="e44a9-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="e44a9-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="e44a9-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="e44a9-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="e44a9-105">Herhaalt een variabele via een Cartesisch product [0, grenzen [0]-1] × [0, grenzen [1]-1] x [0, grenzen [lengte (grenzen)-1]-1] en aanroepen op (arr) voor elk element van het Cartesisch product</span><span class="sxs-lookup"><span data-stu-id="e44a9-105">Iterates a variable through a Cartesian product [ 0, bounds[0]-1 ] × [ 0, bounds[1]-1 ] × [ 0, bounds[Length(bounds)-1]-1 ] and calls op(arr) for every element of the Cartesian product</span></span>

```qsharp
operation _iterateThroughCartesianPower (length : Int, value : Int, op : (Int[] => Unit)) : Unit
```


## <a name="input"></a><span data-ttu-id="e44a9-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="e44a9-106">Input</span></span>

### <a name="length--int"></a><span data-ttu-id="e44a9-107">lengte: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e44a9-107">length : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="value--int"></a><span data-ttu-id="e44a9-108">waarde: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e44a9-108">value : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>




### <a name="op--int--unit"></a><span data-ttu-id="e44a9-109">op: [int](xref:microsoft.quantum.lang-ref.int)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e44a9-109">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 





## <a name="output--unit"></a><span data-ttu-id="e44a9-110">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e44a9-110">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

