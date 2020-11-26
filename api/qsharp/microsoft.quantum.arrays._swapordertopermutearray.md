---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: Functie _SwapOrderToPermuteArray
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: 9df2ec00d91c1124fae960efd15d576b15b0223c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96221705"
---
# <a name="_swapordertopermutearray-function"></a><span data-ttu-id="b67bc-102">Functie _SwapOrderToPermuteArray</span><span class="sxs-lookup"><span data-stu-id="b67bc-102">_SwapOrderToPermuteArray function</span></span>

<span data-ttu-id="b67bc-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="b67bc-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="b67bc-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="b67bc-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="b67bc-105">Retourneert de order elementen in een matrix moeten worden omgewisseld om een geordende matrix te maken.</span><span class="sxs-lookup"><span data-stu-id="b67bc-105">Returns the order elements in an array need to be swapped to produce an ordered array.</span></span>
<span data-ttu-id="b67bc-106">Er wordt van uitgegaan dat er swaps plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="b67bc-106">Assumes swaps occur in place.</span></span>

```qsharp
function _SwapOrderToPermuteArray (newOrder : Int[]) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="b67bc-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="b67bc-107">Input</span></span>

### <a name="neworder--int"></a><span data-ttu-id="b67bc-108">Nieuwebestelling: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="b67bc-108">newOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="b67bc-109">Matrix met de permutatie van de indices van de nieuwe matrix.</span><span class="sxs-lookup"><span data-stu-id="b67bc-109">Array with the permutation of the indices of the new array.</span></span> <span data-ttu-id="b67bc-110">Er moeten $n $-elementen zijn, die elk een uniek geheel getal zijn van $0 $ tot $n-$1.</span><span class="sxs-lookup"><span data-stu-id="b67bc-110">There should be $n$ elements, each being a unique integer from $0$ to $n-1$.</span></span>



## <a name="output--intint"></a><span data-ttu-id="b67bc-111">Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="b67bc-111">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="b67bc-112">De tuple vertegenwoordigt de twee indexen die moeten worden omgewisseld.</span><span class="sxs-lookup"><span data-stu-id="b67bc-112">The tuple represents the two indices to be swapped.</span></span> <span data-ttu-id="b67bc-113">De wissels beginnen bij de laagste index.</span><span class="sxs-lookup"><span data-stu-id="b67bc-113">The swaps begin at the lowest index.</span></span>

## <a name="remarks"></a><span data-ttu-id="b67bc-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="b67bc-114">Remarks</span></span>

## <a name="psuedocode"></a><span data-ttu-id="b67bc-115">Psuedocode</span><span class="sxs-lookup"><span data-stu-id="b67bc-115">Psuedocode</span></span>

<span data-ttu-id="b67bc-116">voor (index in 0.. length (Nieuwebestelling)-1) {while Nieuwebestelling [index]! = index {switch Nieuwebestelling [index] met Nieuwebestelling [Nieuwebestelling [index]]}}</span><span class="sxs-lookup"><span data-stu-id="b67bc-116">for (index in 0..Length(newOrder) - 1) { while newOrder[index] != index { Switch newOrder[index] with newOrder[newOrder[index]] } }</span></span>