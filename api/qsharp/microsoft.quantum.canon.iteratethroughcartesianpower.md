---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Bewerking IterateThroughCartesianPower
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 3a303d13c4a6f102dab92d814e24df9d90213fbe
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98840298"
---
# <a name="iteratethroughcartesianpower-operation"></a><span data-ttu-id="39b80-102">Bewerking IterateThroughCartesianPower</span><span class="sxs-lookup"><span data-stu-id="39b80-102">IterateThroughCartesianPower operation</span></span>

<span data-ttu-id="39b80-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="39b80-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="39b80-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="39b80-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="39b80-105">Past een bewerking toe voor elke index in het Cartesisch vermogen van een bereik met gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="39b80-105">Applies an operation for each index in the Cartesian power of an integer range.</span></span>

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="39b80-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="39b80-106">Description</span></span>

<span data-ttu-id="39b80-107">Hiermee wordt een bewerking uitgevoerd voor elk element van een Cartesisch vermogen van het bereik `0..(bound - 1)` .</span><span class="sxs-lookup"><span data-stu-id="39b80-107">Iteratively applies an operation for each element of a Cartesian power of the range `0..(bound - 1)`.</span></span>

## <a name="input"></a><span data-ttu-id="39b80-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="39b80-108">Input</span></span>

### <a name="power--int"></a><span data-ttu-id="39b80-109">energie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="39b80-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="39b80-110">Het Cartesisch vermogen waarmee het bereik `0..(bound - 1)` moet worden verhoogd.</span><span class="sxs-lookup"><span data-stu-id="39b80-110">The Cartesian power to which the range `0..(bound - 1)` should be raised.</span></span>


### <a name="bound--int"></a><span data-ttu-id="39b80-111">gebonden: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="39b80-111">bound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="39b80-112">Een specificatie van het bereik dat moet worden herhaald, opgegeven als de lengte van het bereik.</span><span class="sxs-lookup"><span data-stu-id="39b80-112">A specification of the range to be iterated over, given as the length of the range.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="39b80-113">op: [int](xref:microsoft.quantum.lang-ref.int)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="39b80-113">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="39b80-114">Een bewerking die moet worden aangeroepen voor elk element van het opgegeven Cartesisch vermogen.</span><span class="sxs-lookup"><span data-stu-id="39b80-114">An operation to be called for each element of the given Cartesian power.</span></span>



## <a name="output--unit"></a><span data-ttu-id="39b80-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="39b80-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="39b80-116">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="39b80-116">Example</span></span>

<span data-ttu-id="39b80-117">Op basis van een bewerking `op` zijn de volgende twee fragmenten gelijk:</span><span class="sxs-lookup"><span data-stu-id="39b80-117">Given an operation `op`, the following two snippets are equivalent:</span></span>

```qsharp
IterateThroughCartesianPower(2, 3, op);
```

```qsharp
op([0, 0]);
op([1, 0]);
op([2, 0]);
op([0, 1]);
// ..
op([2, 2]);
```

## <a name="see-also"></a><span data-ttu-id="39b80-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="39b80-118">See Also</span></span>

- [<span data-ttu-id="39b80-119">Micro soft. Quantum. Canon. IterateThroughCartesianProduct</span><span class="sxs-lookup"><span data-stu-id="39b80-119">Microsoft.Quantum.Canon.IterateThroughCartesianProduct</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)