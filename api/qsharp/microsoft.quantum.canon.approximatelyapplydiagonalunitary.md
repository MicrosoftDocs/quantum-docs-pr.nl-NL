---
uid: Microsoft.Quantum.Canon.ApproximatelyApplyDiagonalUnitary
title: Bewerking ApproximatelyApplyDiagonalUnitary
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyApplyDiagonalUnitary
qsharp.summary: Applies an array of complex phases to numeric basis states of a register of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: 5d8f6646c124f4296b9cd2abd71e73de5a530e55
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850341"
---
# <a name="approximatelyapplydiagonalunitary-operation"></a><span data-ttu-id="8fbed-102">Bewerking ApproximatelyApplyDiagonalUnitary</span><span class="sxs-lookup"><span data-stu-id="8fbed-102">ApproximatelyApplyDiagonalUnitary operation</span></span>

<span data-ttu-id="8fbed-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8fbed-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8fbed-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8fbed-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8fbed-105">Past een matrix van complexe fasen toe op numerieke basis statussen van een REGI ster van qubits, waarbij kleine draai hoeken op basis van een bepaalde tolerantie worden afgekapt.</span><span class="sxs-lookup"><span data-stu-id="8fbed-105">Applies an array of complex phases to numeric basis states of a register of qubits, truncating small rotation angles according to a given tolerance.</span></span>

```qsharp
operation ApproximatelyApplyDiagonalUnitary (tolerance : Double, coefficients : Double[], qubits : Microsoft.Quantum.Arithmetic.LittleEndian) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="8fbed-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8fbed-106">Description</span></span>

<span data-ttu-id="8fbed-107">Met deze bewerking wordt een diagonale unitary geïmplementeerd die een complexe fase $e ^ {i \ theta_j} $ toepast op de $n $-Qubit Number-nummer status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="8fbed-107">This operation implements a diagonal unitary that applies a complex phase $e^{i \theta_j}$ on the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="8fbed-108">Met name deze bewerking kan worden weer gegeven door de unitary</span><span class="sxs-lookup"><span data-stu-id="8fbed-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="8fbed-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} e ^ {i \ theta_j} \ket{j}\bra{j}.</span><span class="sxs-lookup"><span data-stu-id="8fbed-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0}e^{i\theta_j}\ket{j}\bra{j}.</span></span>
<span data-ttu-id="8fbed-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="8fbed-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="8fbed-111">Invoer</span><span class="sxs-lookup"><span data-stu-id="8fbed-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="8fbed-112">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="8fbed-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="8fbed-113">Een tolerantie waaronder kleine coëfficiënten worden afgekapt.</span><span class="sxs-lookup"><span data-stu-id="8fbed-113">A tolerance below which small coefficients are truncated.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="8fbed-114">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="8fbed-114">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="8fbed-115">Matrix van Maxi maal $2 ^ n $ coëfficiënten $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="8fbed-115">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="8fbed-116">De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="8fbed-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="qubits--littleendian"></a><span data-ttu-id="8fbed-117">qubits: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8fbed-117">qubits : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="8fbed-118">$n $-Qubit-controle register dat nummer Staten $ \ket{j} $ codeert in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="8fbed-118">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8fbed-119">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8fbed-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="8fbed-120">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="8fbed-120">Remarks</span></span>

<span data-ttu-id="8fbed-121">`coefficients` wordt aangevuld met elementen $ \ theta_j = $0,0 als er minder dan $2 ^ n $ is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="8fbed-121">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="8fbed-122">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="8fbed-122">References</span></span>

- <span data-ttu-id="8fbed-123">Synthese van Quantum Logic-circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="8fbed-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="8fbed-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8fbed-124">See Also</span></span>

- [<span data-ttu-id="8fbed-125">Micro soft. Quantum. Canon. ApplyDiagonalUnitary</span><span class="sxs-lookup"><span data-stu-id="8fbed-125">Microsoft.Quantum.Canon.ApplyDiagonalUnitary</span></span>](xref:Microsoft.Quantum.Canon.ApplyDiagonalUnitary)