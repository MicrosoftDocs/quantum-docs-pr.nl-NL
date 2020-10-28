---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: Bewerking AssertProbInt
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: a8e4217e18528adc0aa9923f1c0dcfb59e1d2488
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92707437"
---
# <a name="assertprobint-operation"></a><span data-ttu-id="e6996-102">Bewerking AssertProbInt</span><span class="sxs-lookup"><span data-stu-id="e6996-102">AssertProbInt operation</span></span>

<span data-ttu-id="e6996-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="e6996-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="e6996-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="e6996-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="e6996-105">Hiermee wordt bevestigd dat de kans op een specifieke status van een Quantum register de verwachte waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="e6996-105">Asserts that the probability of a specific state of a quantum register has the expected value.</span></span>

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="e6996-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="e6996-106">Description</span></span>

<span data-ttu-id="e6996-107">Gezien een $n $-Qubit Quantum State $ \ket{\psi} = \sum ^ {2 ^ n-1} _ {j = 0} \ alpha_j \ket{j} $, bevestigt u dat de kans $ | \ alpha_j | ^ 2 $ van de status $ \ket{j} $ geïndexeerd door $j $ de verwachte waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="e6996-107">Given an $n$-qubit quantum state $\ket{\psi}=\sum^{2^n-1}_{j=0}\alpha_j \ket{j}$, asserts that the probability $|\alpha_j|^2$ of the state $\ket{j}$ indexed by $j$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="e6996-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="e6996-108">Input</span></span>

### <a name="stateindex--int"></a><span data-ttu-id="e6996-109">stateIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="e6996-109">stateIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="e6996-110">De index $j $ van de status $ \ket{j} $ vertegenwoordigd door een `LittleEndian` REGI ster.</span><span class="sxs-lookup"><span data-stu-id="e6996-110">The index $j$ of the state $\ket{j}$ represented by a `LittleEndian` register.</span></span>


### <a name="expected--double"></a><span data-ttu-id="e6996-111">verwacht: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e6996-111">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e6996-112">De verwachte waarde van $ | \ alpha_j | ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="e6996-112">The expected value of $|\alpha_j|^2$.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="e6996-113">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="e6996-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="e6996-114">Het Qubit-REGI ster waarin $ \ket{\psi} $ wordt opgeslagen in de indeling little-endian.</span><span class="sxs-lookup"><span data-stu-id="e6996-114">The qubit register that stores $\ket{\psi}$ in little-endian format.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="e6996-115">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="e6996-115">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="e6996-116">Absolute tolerantie voor het verschil tussen werkelijk en verwacht.</span><span class="sxs-lookup"><span data-stu-id="e6996-116">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="e6996-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="e6996-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

