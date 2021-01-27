---
uid: Microsoft.Quantum.Canon.ApplyDiagonalUnitary
title: Bewerking ApplyDiagonalUnitary
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyDiagonalUnitary
qsharp.summary: Applies an array of complex phases to numeric basis states of a register of qubits.
ms.openlocfilehash: 14ab8d7beddda26594967225934d472d52bac9eb
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841892"
---
# <a name="applydiagonalunitary-operation"></a><span data-ttu-id="fa81f-102">Bewerking ApplyDiagonalUnitary</span><span class="sxs-lookup"><span data-stu-id="fa81f-102">ApplyDiagonalUnitary operation</span></span>

<span data-ttu-id="fa81f-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fa81f-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fa81f-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="fa81f-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="fa81f-105">Past een matrix van complexe fasen toe op numerieke basis statussen van een REGI ster van qubits.</span><span class="sxs-lookup"><span data-stu-id="fa81f-105">Applies an array of complex phases to numeric basis states of a register of qubits.</span></span>

```qsharp
operation ApplyDiagonalUnitary (coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="fa81f-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="fa81f-106">Description</span></span>

<span data-ttu-id="fa81f-107">Met deze bewerking wordt een diagonale unitary geïmplementeerd die een complexe fase $e ^ {i \ theta_j} $ toepast op de $n $-Qubit Number-nummer status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="fa81f-107">This operation implements a diagonal unitary that applies a complex phase $e^{i \theta_j}$ on the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="fa81f-108">Met name deze bewerking kan worden weer gegeven door de unitary</span><span class="sxs-lookup"><span data-stu-id="fa81f-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="fa81f-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} e ^ {i \ theta_j} \ket{j}\bra{j}.</span><span class="sxs-lookup"><span data-stu-id="fa81f-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0}e^{i\theta_j}\ket{j}\bra{j}.</span></span>
<span data-ttu-id="fa81f-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="fa81f-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="fa81f-111">Invoer</span><span class="sxs-lookup"><span data-stu-id="fa81f-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="fa81f-112">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="fa81f-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="fa81f-113">Matrix van Maxi maal $2 ^ n $ coëfficiënten $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="fa81f-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="fa81f-114">De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="fa81f-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="fa81f-115">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="fa81f-115">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="fa81f-116">$n $-Qubit-controle register dat nummer Staten $ \ket{j} $ codeert in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="fa81f-116">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fa81f-117">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fa81f-117">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="fa81f-118">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="fa81f-118">Remarks</span></span>

<span data-ttu-id="fa81f-119">`coefficients` wordt aangevuld met elementen $ \ theta_j = $0,0 als er minder dan $2 ^ n $ is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="fa81f-119">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="fa81f-120">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="fa81f-120">References</span></span>

- <span data-ttu-id="fa81f-121">Synthese van Quantum Logic-circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="fa81f-121">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="fa81f-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="fa81f-122">See Also</span></span>

- [<span data-ttu-id="fa81f-123">Micro soft. Quantum. Canon. ApproximatelyApplyDiagonalUnitary</span><span class="sxs-lookup"><span data-stu-id="fa81f-123">Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary)