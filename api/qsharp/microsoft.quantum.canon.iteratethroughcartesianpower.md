---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Bewerking IterateThroughCartesianPower
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 526d28cbf3cd356b4f48eec02b3f032f70a868d9
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92704085"
---
# <a name="iteratethroughcartesianpower-operation"></a><span data-ttu-id="51a39-102">Bewerking IterateThroughCartesianPower</span><span class="sxs-lookup"><span data-stu-id="51a39-102">IterateThroughCartesianPower operation</span></span>

<span data-ttu-id="51a39-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="51a39-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="51a39-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="51a39-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="51a39-105">Past een bewerking toe voor elke index in het Cartesisch vermogen van een bereik met gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="51a39-105">Applies an operation for each index in the Cartesian power of an integer range.</span></span>

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="51a39-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="51a39-106">Description</span></span>

<span data-ttu-id="51a39-107">Hiermee wordt een bewerking uitgevoerd voor elk element van een Cartesisch vermogen van het bereik `0..(bound - 1)` .</span><span class="sxs-lookup"><span data-stu-id="51a39-107">Iteratively applies an operation for each element of a Cartesian power of the range `0..(bound - 1)`.</span></span>

## <a name="input"></a><span data-ttu-id="51a39-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="51a39-108">Input</span></span>

### <a name="power--int"></a><span data-ttu-id="51a39-109">energie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="51a39-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="51a39-110">Het Cartesisch vermogen waarmee het bereik `0..(bound - 1)` moet worden verhoogd.</span><span class="sxs-lookup"><span data-stu-id="51a39-110">The Cartesian power to which the range `0..(bound - 1)` should be raised.</span></span>


### <a name="bound--int"></a><span data-ttu-id="51a39-111">gebonden: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="51a39-111">bound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="51a39-112">Een specificatie van het bereik dat moet worden herhaald, opgegeven als de lengte van het bereik.</span><span class="sxs-lookup"><span data-stu-id="51a39-112">A specification of the range to be iterated over, given as the length of the range.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="51a39-113">op: [int](xref:microsoft.quantum.lang-ref.int)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="51a39-113">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="51a39-114">Een bewerking die moet worden aangeroepen voor elk element van het opgegeven Cartesisch vermogen.</span><span class="sxs-lookup"><span data-stu-id="51a39-114">An operation to be called for each element of the given Cartesian power.</span></span>



## <a name="output--unit"></a><span data-ttu-id="51a39-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="51a39-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="51a39-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="51a39-116">See Also</span></span>

- [<span data-ttu-id="51a39-117">Micro soft. Quantum. Canon. IterateThroughCartesianProduct</span><span class="sxs-lookup"><span data-stu-id="51a39-117">Microsoft.Quantum.Canon.IterateThroughCartesianProduct</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)