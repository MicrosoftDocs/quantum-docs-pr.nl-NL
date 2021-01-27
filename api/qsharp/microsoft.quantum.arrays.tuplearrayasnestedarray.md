---
uid: Microsoft.Quantum.Arrays.TupleArrayAsNestedArray
title: De functie TupleArrayAsNestedArray
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: TupleArrayAsNestedArray
qsharp.summary: Turns a list of 2-tuples into a nested array.
ms.openlocfilehash: 51a35555080d1d2475fc1aa9e48e84c7c6f92c51
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98845397"
---
# <a name="tuplearrayasnestedarray-function"></a><span data-ttu-id="a5128-102">De functie TupleArrayAsNestedArray</span><span class="sxs-lookup"><span data-stu-id="a5128-102">TupleArrayAsNestedArray function</span></span>

<span data-ttu-id="a5128-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="a5128-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="a5128-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a5128-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a5128-105">Hiermee wordt een lijst met 2-Tuples omgezet in een geneste matrix.</span><span class="sxs-lookup"><span data-stu-id="a5128-105">Turns a list of 2-tuples into a nested array.</span></span>

```qsharp
function TupleArrayAsNestedArray<'T> (tupleList : ('T, 'T)[]) : 'T[][]
```


## <a name="input"></a><span data-ttu-id="a5128-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="a5128-106">Input</span></span>

### <a name="tuplelist--tt"></a><span data-ttu-id="a5128-107">tupleList: ('T, 'T) []</span><span class="sxs-lookup"><span data-stu-id="a5128-107">tupleList : ('T,'T)[]</span></span>

<span data-ttu-id="a5128-108">Lijst met twee Tuples die moeten worden omgezet in een geneste matrix.</span><span class="sxs-lookup"><span data-stu-id="a5128-108">List of 2-tuples to be turned into a nested array.</span></span>



## <a name="output--t"></a><span data-ttu-id="a5128-109">Uitvoer: ' [] []</span><span class="sxs-lookup"><span data-stu-id="a5128-109">Output : 'T[][]</span></span>

<span data-ttu-id="a5128-110">Een geneste matrix met een lengte die overeenkomt met de tupleList.</span><span class="sxs-lookup"><span data-stu-id="a5128-110">A nested array with length matching the tupleList.</span></span>

## <a name="example"></a><span data-ttu-id="a5128-111">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="a5128-111">Example</span></span>

```qsharp
// The following returns [[2, 3], [4, 5]]
TupleArrayAsNestedArray([(2, 3), (4, 5)]);
```

## <a name="type-parameters"></a><span data-ttu-id="a5128-112">Type parameters</span><span class="sxs-lookup"><span data-stu-id="a5128-112">Type Parameters</span></span>

### <a name="t"></a><span data-ttu-id="a5128-113">T</span><span class="sxs-lookup"><span data-stu-id="a5128-113">'T</span></span>

