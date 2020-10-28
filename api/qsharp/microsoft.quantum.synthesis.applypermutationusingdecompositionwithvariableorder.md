---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder
title: Bewerking ApplyPermutationUsingDecompositionWithVariableOrder
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecompositionWithVariableOrder
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: 1edbc0a2948fdf3ae67f14b3c552676feaa7f498
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92709205"
---
# <a name="applypermutationusingdecompositionwithvariableorder-operation"></a><span data-ttu-id="bef99-102">Bewerking ApplyPermutationUsingDecompositionWithVariableOrder</span><span class="sxs-lookup"><span data-stu-id="bef99-102">ApplyPermutationUsingDecompositionWithVariableOrder operation</span></span>

<span data-ttu-id="bef99-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="bef99-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="bef99-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bef99-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bef99-105">Permutaties de amplitudes in een Quantum status op basis van een permutatie met behulp van op ontleding gebaseerde synthese.</span><span class="sxs-lookup"><span data-stu-id="bef99-105">Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingDecompositionWithVariableOrder (perm : Int[], variableOrder : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="bef99-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="bef99-106">Description</span></span>

<span data-ttu-id="bef99-107">Deze bewerking is een meer algemene versie van waarin @"microsoft.quantum.synthesis.applypermutationusingdecomposition" de variabele volgorde kan worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="bef99-107">This operation is a more general version of @"microsoft.quantum.synthesis.applypermutationusingdecomposition" in which the variable order can be specified.</span></span> <span data-ttu-id="bef99-108">Een andere variabele order wijzigt de ontledings reeks en de waarheids tabellen die worden gebruikt voor de bewaakte @"microsoft.quantum.intrinsic.x" poorten.</span><span class="sxs-lookup"><span data-stu-id="bef99-108">A different variable order changes the decomposition sequence and the truth tables used for the controlled @"microsoft.quantum.intrinsic.x" gates.</span></span>  <span data-ttu-id="bef99-109">Daarom wijzigt de volg orde van de variabele het aantal gebruikte poorten om de permutatie te realiseren.</span><span class="sxs-lookup"><span data-stu-id="bef99-109">Therefore, changing the variable order changes the number of overall gates used to realize the permutation.</span></span>

## <a name="input"></a><span data-ttu-id="bef99-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="bef99-110">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="bef99-111">macht: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="bef99-111">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="bef99-112">Een permutatie van $2 ^ n $ elementen vanaf 0.</span><span class="sxs-lookup"><span data-stu-id="bef99-112">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="variableorder--int"></a><span data-ttu-id="bef99-113">variableOrder: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="bef99-113">variableOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="bef99-114">Een permutatie van $n $ Elements vanaf 0.</span><span class="sxs-lookup"><span data-stu-id="bef99-114">A permutation of $n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="bef99-115">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="bef99-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="bef99-116">Een lijst met $n $ qubits waarop de permutatie wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="bef99-116">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bef99-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bef99-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="bef99-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="bef99-118">See Also</span></span>

- [<span data-ttu-id="bef99-119">Micro soft. Quantum. synthese. ApplyPermutationUsingDecomposition</span><span class="sxs-lookup"><span data-stu-id="bef99-119">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
- [<span data-ttu-id="bef99-120">Micro soft. Quantum. synthese. ApplyPermutationUsingTransformation</span><span class="sxs-lookup"><span data-stu-id="bef99-120">Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)