---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianProduct
title: Bewerking IterateThroughCartesianProduct
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianProduct
qsharp.summary: Applies an operation for each index in the Cartesian product of several ranges.
ms.openlocfilehash: a0aaa8ef6aa6798d31c810254c92820f8136800c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840283"
---
# <a name="iteratethroughcartesianproduct-operation"></a><span data-ttu-id="a7992-102">Bewerking IterateThroughCartesianProduct</span><span class="sxs-lookup"><span data-stu-id="a7992-102">IterateThroughCartesianProduct operation</span></span>

<span data-ttu-id="a7992-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a7992-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a7992-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a7992-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a7992-105">Past een bewerking toe voor elke index in het Cartesisch product van verschillende bereiken.</span><span class="sxs-lookup"><span data-stu-id="a7992-105">Applies an operation for each index in the Cartesian product of several ranges.</span></span>

```qsharp
operation IterateThroughCartesianProduct (bounds : Int[], op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="a7992-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="a7992-106">Description</span></span>

<span data-ttu-id="a7992-107">Hiermee wordt een bewerking uitgevoerd voor elk element van het Cartesisch product van `0..(bounds[0] - 1)` , `0..(bounds[1] - 1)` ,,..., `0..(bounds[Length(bounds) - 1] - 1)`</span><span class="sxs-lookup"><span data-stu-id="a7992-107">Iteratively applies an operation for each element of the Cartesian product of `0..(bounds[0] - 1)`, `0..(bounds[1] - 1)`, ..., `0..(bounds[Length(bounds) - 1] - 1)`</span></span>

## <a name="input"></a><span data-ttu-id="a7992-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="a7992-108">Input</span></span>

### <a name="bounds--int"></a><span data-ttu-id="a7992-109">grenzen: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="a7992-109">bounds : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="a7992-110">Een matrix die de bereiken specificeert die moeten worden herhaald, waarbij elk bereik wordt opgegeven als een integer lengte.</span><span class="sxs-lookup"><span data-stu-id="a7992-110">An array specifying the ranges to be iterated over, with each range being specified as an integer length.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="a7992-111">op: [int](xref:microsoft.quantum.lang-ref.int)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a7992-111">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="a7992-112">Een bewerking die moet worden aangeroepen voor elk element van het opgegeven Cartesisch product.</span><span class="sxs-lookup"><span data-stu-id="a7992-112">An operation to be called for each element of the given Cartesian product.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a7992-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a7992-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="a7992-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="a7992-114">Example</span></span>

<span data-ttu-id="a7992-115">Op basis van een bewerking `op` zijn de volgende twee fragmenten gelijk:</span><span class="sxs-lookup"><span data-stu-id="a7992-115">Given an operation `op`, the following two snippets are equivalent:</span></span>

```qsharp
IterateThroughCartesianProduct([3, 4, 5], op);
```

```qsharp
op([0, 0, 0]);
op([1, 0, 0]);
op([2, 0, 0]);
op([0, 1, 0]);
// ...
op([0, 3, 0]);
op([0, 0, 1]);
//
op([2, 3, 4]);
```

## <a name="see-also"></a><span data-ttu-id="a7992-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a7992-116">See Also</span></span>

- [<span data-ttu-id="a7992-117">Micro soft. Quantum. Canon. IterateThroughCartesianPower</span><span class="sxs-lookup"><span data-stu-id="a7992-117">Microsoft.Quantum.Canon.IterateThroughCartesianPower</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianPower)