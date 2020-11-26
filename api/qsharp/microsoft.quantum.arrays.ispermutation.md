---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: De functie IsPermutation
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 144f683818b5d75de5b075328365d3e994de29d1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96220923"
---
# <a name="ispermutation-function"></a><span data-ttu-id="f27de-102">De functie IsPermutation</span><span class="sxs-lookup"><span data-stu-id="f27de-102">IsPermutation function</span></span>

<span data-ttu-id="f27de-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="f27de-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="f27de-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f27de-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f27de-105">Uitvoer waar als en alleen als een bepaalde matrix een permutatie vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="f27de-105">Outputs true if and only if a given array represents a permutation.</span></span>

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a><span data-ttu-id="f27de-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f27de-106">Description</span></span>

<span data-ttu-id="f27de-107">Met een matrix `array` van lengte `n` retourneert waar als en alleen als elke integer `0` `n - 1` precies één keer in wordt weer gegeven `array` , zodat deze `array` kan worden geïnterpreteerd als een permutatie van `n` elementen.</span><span class="sxs-lookup"><span data-stu-id="f27de-107">Given an array `array` of length `n`, returns true if and only if each integer from `0` to `n - 1` appears exactly once in `array`, such that `array` can be interpreted as a permutation on `n` elements.</span></span>

## <a name="input"></a><span data-ttu-id="f27de-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="f27de-108">Input</span></span>

### <a name="permuation--int"></a><span data-ttu-id="f27de-109">permuation: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="f27de-109">permuation : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="f27de-110">Een matrix die een permutatie kan of mag bevatten.</span><span class="sxs-lookup"><span data-stu-id="f27de-110">An array that may or may not represent a permutation.</span></span>



## <a name="output--bool"></a><span data-ttu-id="f27de-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="f27de-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>



## <a name="remarks"></a><span data-ttu-id="f27de-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="f27de-112">Remarks</span></span>

<span data-ttu-id="f27de-113">Een matrix met een lengte van nul is een permutatie.</span><span class="sxs-lookup"><span data-stu-id="f27de-113">An array of length zero is trivially a permutation.</span></span>