---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: Functie _SwapOrderToPermuteArray
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: 965f2f3d4f8b366abb27287ce0d27a3b7d7b8fb8
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92706189"
---
# <a name="_swapordertopermutearray-function"></a><span data-ttu-id="c4626-102">Functie _SwapOrderToPermuteArray</span><span class="sxs-lookup"><span data-stu-id="c4626-102">_SwapOrderToPermuteArray function</span></span>

<span data-ttu-id="c4626-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="c4626-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="c4626-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="c4626-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="c4626-105">Retourneert de order elementen in een matrix moeten worden omgewisseld om een geordende matrix te maken.</span><span class="sxs-lookup"><span data-stu-id="c4626-105">Returns the order elements in an array need to be swapped to produce an ordered array.</span></span>
<span data-ttu-id="c4626-106">Er wordt van uitgegaan dat er swaps plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="c4626-106">Assumes swaps occur in place.</span></span>

```qsharp
function _SwapOrderToPermuteArray (newOrder : Int[]) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="c4626-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="c4626-107">Input</span></span>

### <a name="neworder--int"></a><span data-ttu-id="c4626-108">Nieuwebestelling: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="c4626-108">newOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="c4626-109">Matrix met de permutatie van de indices van de nieuwe matrix.</span><span class="sxs-lookup"><span data-stu-id="c4626-109">Array with the permutation of the indices of the new array.</span></span> <span data-ttu-id="c4626-110">Er moeten $n $-elementen zijn, die elk een uniek geheel getal zijn van $0 $ tot $n-$1.</span><span class="sxs-lookup"><span data-stu-id="c4626-110">There should be $n$ elements, each being a unique integer from $0$ to $n-1$.</span></span>



## <a name="output--intint"></a><span data-ttu-id="c4626-111">Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="c4626-111">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="c4626-112">De tuple vertegenwoordigt de twee indexen die moeten worden omgewisseld.</span><span class="sxs-lookup"><span data-stu-id="c4626-112">The tuple represents the two indices to be swapped.</span></span> <span data-ttu-id="c4626-113">De wissels beginnen bij de laagste index.</span><span class="sxs-lookup"><span data-stu-id="c4626-113">The swaps begin at the lowest index.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4626-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="c4626-114">Remarks</span></span>

## <a name="psuedocode"></a><span data-ttu-id="c4626-115">Psuedocode</span><span class="sxs-lookup"><span data-stu-id="c4626-115">Psuedocode</span></span>

<span data-ttu-id="c4626-116">voor (index in 0.. length (Nieuwebestelling)-1) {while Nieuwebestelling [index]! = index {switch Nieuwebestelling [index] met Nieuwebestelling [Nieuwebestelling [index]]}}</span><span class="sxs-lookup"><span data-stu-id="c4626-116">for (index in 0..Length(newOrder) - 1) { while newOrder[index] != index { Switch newOrder[index] with newOrder[newOrder[index]] } }</span></span>