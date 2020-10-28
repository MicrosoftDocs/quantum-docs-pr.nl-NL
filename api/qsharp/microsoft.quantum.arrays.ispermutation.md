---
uid: Microsoft.Quantum.Arrays.IsPermutation
title: De functie IsPermutation
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: function
qsharp.namespace: Microsoft.Quantum.Arrays
qsharp.name: IsPermutation
qsharp.summary: Outputs true if and only if a given array represents a permutation.
ms.openlocfilehash: 361bb21bedc725c25a1f3dfc811e9cfda4cb45ff
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705933"
---
# <a name="ispermutation-function"></a><span data-ttu-id="9f9b2-102">De functie IsPermutation</span><span class="sxs-lookup"><span data-stu-id="9f9b2-102">IsPermutation function</span></span>

<span data-ttu-id="9f9b2-103">Naam ruimte: [micro soft. Quantum. arrays](xref:Microsoft.Quantum.Arrays)</span><span class="sxs-lookup"><span data-stu-id="9f9b2-103">Namespace: [Microsoft.Quantum.Arrays](xref:Microsoft.Quantum.Arrays)</span></span>

<span data-ttu-id="9f9b2-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="9f9b2-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="9f9b2-105">Uitvoer waar als en alleen als een bepaalde matrix een permutatie vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-105">Outputs true if and only if a given array represents a permutation.</span></span>

```qsharp
function IsPermutation (permuation : Int[]) : Bool
```


## <a name="description"></a><span data-ttu-id="9f9b2-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="9f9b2-106">Description</span></span>

<span data-ttu-id="9f9b2-107">Met een matrix `array` van lengte `n` retourneert waar als en alleen als elke integer `0` `n - 1` precies één keer in wordt weer gegeven `array` , zodat deze `array` kan worden geïnterpreteerd als een permutatie van `n` elementen.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-107">Given an array `array` of length `n`, returns true if and only if each integer from `0` to `n - 1` appears exactly once in `array`, such that `array` can be interpreted as a permutation on `n` elements.</span></span>

## <a name="input"></a><span data-ttu-id="9f9b2-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="9f9b2-108">Input</span></span>

### <a name="permuation--int"></a><span data-ttu-id="9f9b2-109">permuation: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="9f9b2-109">permuation : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="9f9b2-110">Een matrix die een permutatie kan of mag bevatten.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-110">An array that may or may not represent a permutation.</span></span>



## <a name="output--bool"></a><span data-ttu-id="9f9b2-111">Uitvoer: [BOOL](xref:microsoft.quantum.lang-ref.bool)</span><span class="sxs-lookup"><span data-stu-id="9f9b2-111">Output : [Bool](xref:microsoft.quantum.lang-ref.bool)</span></span>



## <a name="remarks"></a><span data-ttu-id="9f9b2-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="9f9b2-112">Remarks</span></span>

<span data-ttu-id="9f9b2-113">Een matrix met een lengte van nul is een permutatie.</span><span class="sxs-lookup"><span data-stu-id="9f9b2-113">An array of length zero is trivially a permutation.</span></span>