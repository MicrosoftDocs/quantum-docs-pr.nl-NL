---
uid: Microsoft.Quantum.Canon.IterateThroughCartesianPower
title: Bewerking IterateThroughCartesianPower
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: IterateThroughCartesianPower
qsharp.summary: Applies an operation for each index in the Cartesian power of an integer range.
ms.openlocfilehash: 2883e7cb30633afe51d380befe806665207c5abd
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206473"
---
# <a name="iteratethroughcartesianpower-operation"></a><span data-ttu-id="f1c75-102">Bewerking IterateThroughCartesianPower</span><span class="sxs-lookup"><span data-stu-id="f1c75-102">IterateThroughCartesianPower operation</span></span>

<span data-ttu-id="f1c75-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="f1c75-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="f1c75-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f1c75-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f1c75-105">Past een bewerking toe voor elke index in het Cartesisch vermogen van een bereik met gehele getallen.</span><span class="sxs-lookup"><span data-stu-id="f1c75-105">Applies an operation for each index in the Cartesian power of an integer range.</span></span>

```qsharp
operation IterateThroughCartesianPower (power : Int, bound : Int, op : (Int[] => Unit)) : Unit
```


## <a name="description"></a><span data-ttu-id="f1c75-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f1c75-106">Description</span></span>

<span data-ttu-id="f1c75-107">Hiermee wordt een bewerking uitgevoerd voor elk element van een Cartesisch vermogen van het bereik `0..(bound - 1)` .</span><span class="sxs-lookup"><span data-stu-id="f1c75-107">Iteratively applies an operation for each element of a Cartesian power of the range `0..(bound - 1)`.</span></span>

## <a name="input"></a><span data-ttu-id="f1c75-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="f1c75-108">Input</span></span>

### <a name="power--int"></a><span data-ttu-id="f1c75-109">energie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f1c75-109">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f1c75-110">Het Cartesisch vermogen waarmee het bereik `0..(bound - 1)` moet worden verhoogd.</span><span class="sxs-lookup"><span data-stu-id="f1c75-110">The Cartesian power to which the range `0..(bound - 1)` should be raised.</span></span>


### <a name="bound--int"></a><span data-ttu-id="f1c75-111">gebonden: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f1c75-111">bound : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f1c75-112">Een specificatie van het bereik dat moet worden herhaald, opgegeven als de lengte van het bereik.</span><span class="sxs-lookup"><span data-stu-id="f1c75-112">A specification of the range to be iterated over, given as the length of the range.</span></span>


### <a name="op--int--unit"></a><span data-ttu-id="f1c75-113">op: [int](xref:microsoft.quantum.lang-ref.int)[] => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f1c75-113">op : [Int](xref:microsoft.quantum.lang-ref.int)[] => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="f1c75-114">Een bewerking die moet worden aangeroepen voor elk element van het opgegeven Cartesisch vermogen.</span><span class="sxs-lookup"><span data-stu-id="f1c75-114">An operation to be called for each element of the given Cartesian power.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f1c75-115">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f1c75-115">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="f1c75-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f1c75-116">See Also</span></span>

- [<span data-ttu-id="f1c75-117">Micro soft. Quantum. Canon. IterateThroughCartesianProduct</span><span class="sxs-lookup"><span data-stu-id="f1c75-117">Microsoft.Quantum.Canon.IterateThroughCartesianProduct</span></span>](xref:Microsoft.Quantum.Canon.IterateThroughCartesianProduct)