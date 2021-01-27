---
uid: Microsoft.Quantum.Canon.MultiplexZ
title: Bewerking MultiplexZ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexZ
qsharp.summary: Applies a Pauli Z rotation conditioned on an array of qubits.
ms.openlocfilehash: dccfe86104263e23794bce33279e8748f11f5a54
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98852431"
---
# <a name="multiplexz-operation"></a><span data-ttu-id="8da28-102">Bewerking MultiplexZ</span><span class="sxs-lookup"><span data-stu-id="8da28-102">MultiplexZ operation</span></span>

<span data-ttu-id="8da28-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="8da28-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="8da28-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="8da28-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="8da28-105">Hiermee wordt een Pauli Z-rotatie toegepast op een matrix van qubits.</span><span class="sxs-lookup"><span data-stu-id="8da28-105">Applies a Pauli Z rotation conditioned on an array of qubits.</span></span>

```qsharp
operation MultiplexZ (coefficients : Double[], control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="8da28-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="8da28-106">Description</span></span>

<span data-ttu-id="8da28-107">Hiermee wordt de unitary-bewerking met vermenigvuldiging toegepast waarmee rotaties worden uitgevoerd op basis van hoek $ \ theta_j $ over een Qubit Pauli-operator $Z $, wanneer deze wordt beheerd door de $n $-Qubit nummer status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="8da28-107">This applies the multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $Z$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="8da28-108">Met name deze bewerking kan worden weer gegeven door de unitary</span><span class="sxs-lookup"><span data-stu-id="8da28-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="8da28-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i Z \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="8da28-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0} \ket{j}\bra{j} \otimes e^{i Z \theta_j}.</span></span>
<span data-ttu-id="8da28-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="8da28-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="8da28-111">Invoer</span><span class="sxs-lookup"><span data-stu-id="8da28-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="8da28-112">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="8da28-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="8da28-113">Matrix van Maxi maal $2 ^ n $ coëfficiënten $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="8da28-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="8da28-114">De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="8da28-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="8da28-115">besturings element: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="8da28-115">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="8da28-116">$n $-Qubit-controle register dat nummer Staten $ \ket{j} $ codeert in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="8da28-116">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="8da28-117">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="8da28-117">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="8da28-118">Een single Qubit-REGI ster dat wordt geroteerd door $e ^ {i P \ theta_j} $.</span><span class="sxs-lookup"><span data-stu-id="8da28-118">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="8da28-119">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="8da28-119">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="8da28-120">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="8da28-120">Remarks</span></span>

<span data-ttu-id="8da28-121">`coefficients` wordt aangevuld met elementen $ \ theta_j = $0,0 als er minder dan $2 ^ n $ is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="8da28-121">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="8da28-122">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="8da28-122">References</span></span>

- <span data-ttu-id="8da28-123">Synthese van Quantum Logic-circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="8da28-123">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="8da28-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8da28-124">See Also</span></span>

- [<span data-ttu-id="8da28-125">Micro soft. Quantum. Canon. ApproximatelyMultiplexZ</span><span class="sxs-lookup"><span data-stu-id="8da28-125">Microsoft.Quantum.Canon.ApproximatelyMultiplexZ</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyMultiplexZ)