---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: De functie IsPermutation
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 7e563650f33b0292e1e41f629829a2d3b9e5fd28
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98848099"
---
# <a name="ispermutation-function"></a><span data-ttu-id="2ce6d-102">De functie IsPermutation</span><span class="sxs-lookup"><span data-stu-id="2ce6d-102">IsPermutation function</span></span>

<span data-ttu-id="2ce6d-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="2ce6d-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="2ce6d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="2ce6d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="2ce6d-105">Uitvoer waar als en alleen als een bepaalde matrix een permutatie vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="2ce6d-105">Outputs true if and only if a given array represents a permutation.</span></span>

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a><span data-ttu-id="2ce6d-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="2ce6d-106">Description</span></span>

<span data-ttu-id="2ce6d-107">Met een matrix `array` van lengte `n` retourneert waar als en alleen als elke integer `0` `n - 1` precies één keer in wordt weer gegeven `array` , zodat deze `array` kan worden geïnterpreteerd als een permutatie van `n` elementen.</span><span class="sxs-lookup"><span data-stu-id="2ce6d-107">Given an array `array` of length `n`, returns true if and only if each integer from `0` to `n - 1` appears exactly once in `array`, such that `array` can be interpreted as a permutation on `n` elements.</span></span>

## <a name="input"></a><span data-ttu-id="2ce6d-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="2ce6d-108">Input</span></span>

### <a name="permuation--int"></a><span data-ttu-id="2ce6d-109">permuation: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="2ce6d-109">permuation : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="2ce6d-110">Een matrix die een permutatie kan of mag bevatten.</span><span class="sxs-lookup"><span data-stu-id="2ce6d-110">An array that may or may not represent a permutation.</span></span>



## <a name="output--bool"></a><span data-ttu-id="2ce6d-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="2ce6d-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>



## <a name="example"></a><span data-ttu-id="2ce6d-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="2ce6d-112">Example</span></span>

<span data-ttu-id="2ce6d-113">Met de volgende Q #-code wordt het bericht ' alle diagnostische gegevens zijn voltooid ' afgedrukt:</span><span class="sxs-lookup"><span data-stu-id="2ce6d-113">The following Q# code prints the message "All diagnostics completed successfully":</span></span>

```qsharp
Fact(IsPermutation([2, 0, 1], "");
Contradiction(IsPermutation([5, 0, 1], "[5, 0, 1] isn't a permutation");
Message("All diagnostics completed successfully.");
```

## <a name="remarks"></a><span data-ttu-id="2ce6d-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="2ce6d-114">Remarks</span></span>

<span data-ttu-id="2ce6d-115">Een matrix met een lengte van nul is een permutatie.</span><span class="sxs-lookup"><span data-stu-id="2ce6d-115">An array of length zero is trivially a permutation.</span></span>