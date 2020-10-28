---
uid: Microsoft.Quantum.Canon.ApplyDiagonalUnitary
title: Bewerking ApplyDiagonalUnitary
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyDiagonalUnitary
qsharp.summary: Applies an array of complex phases to numeric basis states of a register of qubits.
ms.openlocfilehash: 6ecacf6e4fe2c505036de208c8aeb5350e479e3c
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705388"
---
# <a name="applydiagonalunitary-operation"></a><span data-ttu-id="77ca5-102">Bewerking ApplyDiagonalUnitary</span><span class="sxs-lookup"><span data-stu-id="77ca5-102">ApplyDiagonalUnitary operation</span></span>

<span data-ttu-id="77ca5-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="77ca5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="77ca5-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="77ca5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="77ca5-105">Past een matrix van complexe fasen toe op numerieke basis statussen van een REGI ster van qubits.</span><span class="sxs-lookup"><span data-stu-id="77ca5-105">Applies an array of complex phases to numeric basis states of a register of qubits.</span></span>

```qsharp
operation ApplyDiagonalUnitary (coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit
```


## <a name="description"></a><span data-ttu-id="77ca5-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="77ca5-106">Description</span></span>

<span data-ttu-id="77ca5-107">Met deze bewerking wordt een diagonale unitary geïmplementeerd die een complexe fase $e ^ {i \ theta_j} $ toepast op de $n $-Qubit Number-nummer status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="77ca5-107">This operation implements a diagonal unitary that applies a complex phase $e^{i \theta_j}$ on the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="77ca5-108">Met name deze bewerking kan worden weer gegeven door de unitary</span><span class="sxs-lookup"><span data-stu-id="77ca5-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="77ca5-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} e ^ {i \ theta_j} \ket{j}\bra{j}.</span><span class="sxs-lookup"><span data-stu-id="77ca5-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0}e^{i\theta_j}\ket{j}\bra{j}.</span></span>
<span data-ttu-id="77ca5-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="77ca5-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="77ca5-111">Invoer</span><span class="sxs-lookup"><span data-stu-id="77ca5-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="77ca5-112">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="77ca5-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="77ca5-113">Matrix van Maxi maal $2 ^ n $ coëfficiënten $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="77ca5-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="77ca5-114">De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="77ca5-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="77ca5-115">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="77ca5-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="77ca5-116">$n $-Qubit-controle register dat nummer Staten $ \ket{j} $ codeert in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="77ca5-116">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="77ca5-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="77ca5-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="77ca5-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="77ca5-118">Remarks</span></span>

<span data-ttu-id="77ca5-119">`coefficients` wordt aangevuld met elementen $ \ theta_j = $0,0 als er minder dan $2 ^ n $ is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="77ca5-119">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="77ca5-120">Naslaginformatie</span><span class="sxs-lookup"><span data-stu-id="77ca5-120">References</span></span>

- <span data-ttu-id="77ca5-121">Synthese van Quantum Logic-circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="77ca5-121">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="77ca5-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="77ca5-122">See Also</span></span>

- [<span data-ttu-id="77ca5-123">Micro soft. Quantum. Canon. ApproximatelyApplyDiagonalUnitary</span><span class="sxs-lookup"><span data-stu-id="77ca5-123">Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary)