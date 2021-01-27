---
uid: Microsoft.Quantum.Arithmetic.AssertProbInt
title: Bewerking AssertProbInt
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Arithmetic
qsharp.name: AssertProbInt
qsharp.summary: Asserts that the probability of a specific state of a quantum register has the expected value.
ms.openlocfilehash: 85ff04bbad9dc2ed0f803db65508fdfbb0d22c56
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98843409"
---
# <a name="assertprobint-operation"></a><span data-ttu-id="f80c1-102">Bewerking AssertProbInt</span><span class="sxs-lookup"><span data-stu-id="f80c1-102">AssertProbInt operation</span></span>

<span data-ttu-id="f80c1-103">Naam ruimte: [micro soft. Quantum. aritmetische](xref:Microsoft.Quantum.Arithmetic)</span><span class="sxs-lookup"><span data-stu-id="f80c1-103">Namespace: [Microsoft.Quantum.Arithmetic](xref:Microsoft.Quantum.Arithmetic)</span></span>

<span data-ttu-id="f80c1-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="f80c1-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="f80c1-105">Hiermee wordt bevestigd dat de kans op een specifieke status van een Quantum register de verwachte waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="f80c1-105">Asserts that the probability of a specific state of a quantum register has the expected value.</span></span>

```qsharp
operation AssertProbInt (stateIndex : Int, expected : Double, qubits : Microsoft.Quantum.Arithmetic.LittleEndian, tolerance : Double) : Unit
```


## <a name="description"></a><span data-ttu-id="f80c1-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f80c1-106">Description</span></span>

<span data-ttu-id="f80c1-107">Gezien een $n $-Qubit Quantum State $ \ket{\psi} = \sum ^ {2 ^ n-1} _ {j = 0} \ alpha_j \ket{j} $, bevestigt u dat de kans $ | \ alpha_j | ^ 2 $ van de status $ \ket{j} $ geïndexeerd door $j $ de verwachte waarde heeft.</span><span class="sxs-lookup"><span data-stu-id="f80c1-107">Given an $n$-qubit quantum state $\ket{\psi}=\sum^{2^n-1}_{j=0}\alpha_j \ket{j}$, asserts that the probability $|\alpha_j|^2$ of the state $\ket{j}$ indexed by $j$ has the expected value.</span></span>

## <a name="input"></a><span data-ttu-id="f80c1-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="f80c1-108">Input</span></span>

### <a name="stateindex--int"></a><span data-ttu-id="f80c1-109">stateIndex: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="f80c1-109">stateIndex : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="f80c1-110">De index $j $ van de status $ \ket{j} $ vertegenwoordigd door een `LittleEndian` REGI ster.</span><span class="sxs-lookup"><span data-stu-id="f80c1-110">The index $j$ of the state $\ket{j}$ represented by a `LittleEndian` register.</span></span>


### <a name="expected--double"></a><span data-ttu-id="f80c1-111">verwacht: [Double](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f80c1-111">expected : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f80c1-112">De verwachte waarde van $ | \ alpha_j | ^ 2 $.</span><span class="sxs-lookup"><span data-stu-id="f80c1-112">The expected value of $|\alpha_j|^2$.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="f80c1-113">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="f80c1-113">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="f80c1-114">Het Qubit-REGI ster waarin $ \ket{\psi} $ wordt opgeslagen in de indeling little-endian.</span><span class="sxs-lookup"><span data-stu-id="f80c1-114">The qubit register that stores $\ket{\psi}$ in little-endian format.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="f80c1-115">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="f80c1-115">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="f80c1-116">Absolute tolerantie voor het verschil tussen werkelijk en verwacht.</span><span class="sxs-lookup"><span data-stu-id="f80c1-116">Absolute tolerance on the difference between actual and expected.</span></span>



## <a name="output--unit"></a><span data-ttu-id="f80c1-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="f80c1-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="f80c1-118">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="f80c1-118">Example</span></span>

<span data-ttu-id="f80c1-119">Stel dat het `qubits` REGI ster een 3-Qubit Quantum State $ \ket{\psi} = \ SQRT {1/8} \ Ket {0} + \ SQRT {7/8} \ Ket {6} $ in de indeling little endian codeert.</span><span class="sxs-lookup"><span data-stu-id="f80c1-119">Suppose that the `qubits` register encodes a 3-qubit quantum state $\ket{\psi}=\sqrt{1/8}\ket{0}+\sqrt{7/8}\ket{6}$ in little-endian format.</span></span>
<span data-ttu-id="f80c1-120">Dit betekent dat het aantal statussen $ \ket {0} \equiv\ket {0} \ket {0} \ket {0} $ en $ \ket \equiv\ket \ket \ket {6} {0} {1} {1} $.</span><span class="sxs-lookup"><span data-stu-id="f80c1-120">This means that the number states $\ket{0}\equiv\ket{0}\ket{0}\ket{0}$ and $\ket{6}\equiv\ket{0}\ket{1}\ket{1}$.</span></span> <span data-ttu-id="f80c1-121">Daarna slagen de volgende verklaringen:</span><span class="sxs-lookup"><span data-stu-id="f80c1-121">Then the following asserts succeed:</span></span>

```qsharp
AssertProbInt(0, 0.125, qubits, 10e-10);
AssertProbInt(6, 0.875, qubits, 10e-10);
```