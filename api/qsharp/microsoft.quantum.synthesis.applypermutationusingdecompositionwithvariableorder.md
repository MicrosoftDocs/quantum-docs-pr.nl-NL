---
uid: Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecompositionWithVariableOrder
title: Bewerking ApplyPermutationUsingDecompositionWithVariableOrder
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Synthesis
qsharp.name: ApplyPermutationUsingDecompositionWithVariableOrder
qsharp.summary: Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.
ms.openlocfilehash: a5ca9b366f7ff477070e21fea047ff04b425439c
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96203430"
---
# <a name="applypermutationusingdecompositionwithvariableorder-operation"></a><span data-ttu-id="07faa-102">Bewerking ApplyPermutationUsingDecompositionWithVariableOrder</span><span class="sxs-lookup"><span data-stu-id="07faa-102">ApplyPermutationUsingDecompositionWithVariableOrder operation</span></span>

<span data-ttu-id="07faa-103">Naam ruimte: [micro soft. Quantum. synthese](xref:Microsoft.Quantum.Synthesis)</span><span class="sxs-lookup"><span data-stu-id="07faa-103">Namespace: [Microsoft.Quantum.Synthesis](xref:Microsoft.Quantum.Synthesis)</span></span>

<span data-ttu-id="07faa-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="07faa-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="07faa-105">Permutaties de amplitudes in een Quantum status op basis van een permutatie met behulp van op ontleding gebaseerde synthese.</span><span class="sxs-lookup"><span data-stu-id="07faa-105">Permutes the amplitudes in a quantum state given a permutation using decomposition-based synthesis.</span></span>

```qsharp
operation ApplyPermutationUsingDecompositionWithVariableOrder (perm : Int[], variableOrder : Int[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="07faa-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="07faa-106">Description</span></span>

<span data-ttu-id="07faa-107">Deze bewerking is een meer algemene versie van waarin @"microsoft.quantum.synthesis.applypermutationusingdecomposition" de variabele volgorde kan worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="07faa-107">This operation is a more general version of @"microsoft.quantum.synthesis.applypermutationusingdecomposition" in which the variable order can be specified.</span></span> <span data-ttu-id="07faa-108">Een andere variabele order wijzigt de ontledings reeks en de waarheids tabellen die worden gebruikt voor de bewaakte @"microsoft.quantum.intrinsic.x" poorten.</span><span class="sxs-lookup"><span data-stu-id="07faa-108">A different variable order changes the decomposition sequence and the truth tables used for the controlled @"microsoft.quantum.intrinsic.x" gates.</span></span>  <span data-ttu-id="07faa-109">Daarom wijzigt de volg orde van de variabele het aantal gebruikte poorten om de permutatie te realiseren.</span><span class="sxs-lookup"><span data-stu-id="07faa-109">Therefore, changing the variable order changes the number of overall gates used to realize the permutation.</span></span>

## <a name="input"></a><span data-ttu-id="07faa-110">Invoer</span><span class="sxs-lookup"><span data-stu-id="07faa-110">Input</span></span>

### <a name="perm--int"></a><span data-ttu-id="07faa-111">macht: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="07faa-111">perm : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="07faa-112">Een permutatie van $2 ^ n $ elementen vanaf 0.</span><span class="sxs-lookup"><span data-stu-id="07faa-112">A permutation of $2^n$ elements starting from 0.</span></span>


### <a name="variableorder--int"></a><span data-ttu-id="07faa-113">variableOrder: [int](xref:microsoft.quantum.lang-ref.int)[]</span><span class="sxs-lookup"><span data-stu-id="07faa-113">variableOrder : [Int](xref:microsoft.quantum.lang-ref.int)[]</span></span>

<span data-ttu-id="07faa-114">Een permutatie van $n $ Elements vanaf 0.</span><span class="sxs-lookup"><span data-stu-id="07faa-114">A permutation of $n$ elements starting from 0.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="07faa-115">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="07faa-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="07faa-116">Een lijst met $n $ qubits waarop de permutatie wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="07faa-116">A list of $n$ qubits to which the permutation is applied to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="07faa-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="07faa-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="07faa-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="07faa-118">See Also</span></span>

- [<span data-ttu-id="07faa-119">Micro soft. Quantum. synthese. ApplyPermutationUsingDecomposition</span><span class="sxs-lookup"><span data-stu-id="07faa-119">Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingDecomposition)
- [<span data-ttu-id="07faa-120">Micro soft. Quantum. synthese. ApplyPermutationUsingTransformation</span><span class="sxs-lookup"><span data-stu-id="07faa-120">Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation</span></span>](xref:Microsoft.Quantum.Synthesis.ApplyPermutationUsingTransformation)