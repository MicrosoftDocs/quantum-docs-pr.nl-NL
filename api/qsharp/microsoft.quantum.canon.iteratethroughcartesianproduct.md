---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: Bewerking IterateThroughCartesianProduct
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: 6340c7a972253e6f583a3856df93a7066ced3139
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206439"
---
# <a name="iteratethroughcartesianproduct-operation"></a><span data-ttu-id="ac760-102">Bewerking IterateThroughCartesianProduct</span><span class="sxs-lookup"><span data-stu-id="ac760-102">IterateThroughCartesianProduct operation</span></span>

<span data-ttu-id="ac760-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ac760-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ac760-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ac760-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ac760-105">Past een bewerking toe voor elke index in het Cartesisch product van verschillende bereiken.</span><span class="sxs-lookup"><span data-stu-id="ac760-105">Applies an operation for each index in the Cartesian product of several ranges.</span></span>

```qsharp
operation IterateThroughCartesianProduct (bounds : Int[], op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="ac760-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ac760-106">Description</span></span>

<span data-ttu-id="ac760-107">Hiermee wordt een bewerking uitgevoerd voor elk element van het Cartesisch product van `0..(bounds[0] - 1)` , `0..(bounds[1] - 1)` ,,..., `0..(bounds[Length(bounds) - 1] - 1)`</span><span class="sxs-lookup"><span data-stu-id="ac760-107">Iteratively applies an operation for each element of the Cartesian product of `0..(bounds[0] - 1)`, `0..(bounds[1] - 1)`, ..., `0..(bounds[Length(bounds) - 1] - 1)`</span></span>

## <a name="input"></a><span data-ttu-id="ac760-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="ac760-108">Input</span></span>

### <a name="bounds--int"></a><span data-ttu-id="ac760-109">grenzen: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="ac760-109">bounds : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="ac760-110">Een matrix die de bereiken specificeert die moeten worden herhaald, waarbij elk bereik wordt opgegeven als een integer lengte.</span><span class="sxs-lookup"><span data-stu-id="ac760-110">An array specifying the ranges to be iterated over, with each range being specified as an integer length.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="ac760-111">op: [int](xref:microsoft.quantum.lang-ref.int)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ac760-111">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="ac760-112">Een bewerking die moet worden aangeroepen voor elk element van het opgegeven Cartesisch product.</span><span class="sxs-lookup"><span data-stu-id="ac760-112">An operation to be called for each element of the given Cartesian product.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ac760-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ac760-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="ac760-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ac760-114">See Also</span></span>

- [<span data-ttu-id="ac760-115">Micro soft. Quantum. Canon. IterateThroughCartesianPower</span><span class="sxs-lookup"><span data-stu-id="ac760-115">Microsoft.Quantum.Canon.IterateThroughCartesianPower</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)