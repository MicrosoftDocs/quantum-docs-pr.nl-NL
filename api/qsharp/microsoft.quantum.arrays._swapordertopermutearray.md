---
uid: Microsoft.Quantum.Arrays._SwapOrderToPermuteArray
title: Functie _SwapOrderToPermuteArray
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: _SwapOrderToPermuteArray
qsharp.summary: Returns the order elements in an array need to be swapped to produce an ordered array. Assumes swaps occur in place.
ms.openlocfilehash: ff8e4e23dde7d69f93054a275548ded49d5b0bfb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98846296"
---
# <a name="_swapordertopermutearray-function"></a><span data-ttu-id="801db-102">Functie _SwapOrderToPermuteArray</span><span class="sxs-lookup"><span data-stu-id="801db-102">_SwapOrderToPermuteArray function</span></span>

<span data-ttu-id="801db-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="801db-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="801db-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="801db-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="801db-105">Retourneert de order elementen in een matrix moeten worden omgewisseld om een geordende matrix te maken.</span><span class="sxs-lookup"><span data-stu-id="801db-105">Returns the order elements in an array need to be swapped to produce an ordered array.</span></span>
<span data-ttu-id="801db-106">Er wordt van uitgegaan dat er swaps plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="801db-106">Assumes swaps occur in place.</span></span>

```qsharp
function _SwapOrderToPermuteArray (newOrder : Int[]) : (Int, Int)[]
```


## <a name="input"></a><span data-ttu-id="801db-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="801db-107">Input</span></span>

### <a name="neworder--int"></a><span data-ttu-id="801db-108">Nieuwebestelling: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="801db-108">newOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="801db-109">Matrix met de permutatie van de indices van de nieuwe matrix.</span><span class="sxs-lookup"><span data-stu-id="801db-109">Array with the permutation of the indices of the new array.</span></span> <span data-ttu-id="801db-110">Er moeten $n $-elementen zijn, die elk een uniek geheel getal zijn van $0 $ tot $n-$1.</span><span class="sxs-lookup"><span data-stu-id="801db-110">There should be $n$ elements, each being a unique integer from $0$ to $n-1$.</span></span>



## <a name="output--intint"></a><span data-ttu-id="801db-111">Uitvoer: ([int](xref:microsoft.quantum.lang-ref.int),[int](xref:microsoft.quantum.lang-ref.int)) []</span><span class="sxs-lookup"><span data-stu-id="801db-111">Output : ([Int](xref:microsoft.quantum.lang-ref.int),[Int](xref:microsoft.quantum.lang-ref.int))[]</span></span>

<span data-ttu-id="801db-112">De tuple vertegenwoordigt de twee indexen die moeten worden omgewisseld.</span><span class="sxs-lookup"><span data-stu-id="801db-112">The tuple represents the two indices to be swapped.</span></span> <span data-ttu-id="801db-113">De wissels beginnen bij de laagste index.</span><span class="sxs-lookup"><span data-stu-id="801db-113">The swaps begin at the lowest index.</span></span>

## <a name="example"></a><span data-ttu-id="801db-114">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="801db-114">Example</span></span>

```qsharp
// The following returns [(0, 5),(0, 4),(0, 1),(0, 3)];
let swapOrder = _SwapOrderToPermuteArray([5, 3, 2, 0, 1, 4]);
```

## <a name="remarks"></a><span data-ttu-id="801db-115">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="801db-115">Remarks</span></span>

## <a name="psuedocode"></a><span data-ttu-id="801db-116">Psuedocode</span><span class="sxs-lookup"><span data-stu-id="801db-116">Psuedocode</span></span>

<span data-ttu-id="801db-117">voor (index in 0.. length (Nieuwebestelling)-1) {while Nieuwebestelling [index]! = index {switch Nieuwebestelling [index] met Nieuwebestelling [Nieuwebestelling [index]]}}</span><span class="sxs-lookup"><span data-stu-id="801db-117">for (index in 0..Length(newOrder) - 1) { while newOrder[index] != index { Switch newOrder[index] with newOrder[newOrder[index]] } }</span></span>