---
uid: Microsoft.Quantum.Canon.MultiplexPauli
title: Bewerking MultiplexPauli
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: MultiplexPauli
qsharp.summary: Applies a Pauli rotation conditioned on an array of qubits.
ms.openlocfilehash: c29f7efa6b10835ce41ca4c535ec1371ac38ab63
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96206030"
---
# <a name="multiplexpauli-operation"></a><span data-ttu-id="bc854-102">Bewerking MultiplexPauli</span><span class="sxs-lookup"><span data-stu-id="bc854-102">MultiplexPauli operation</span></span>

<span data-ttu-id="bc854-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="bc854-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="bc854-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="bc854-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="bc854-105">Hiermee wordt een Pauli-rotatie toegepast op een matrix van qubits.</span><span class="sxs-lookup"><span data-stu-id="bc854-105">Applies a Pauli rotation conditioned on an array of qubits.</span></span>

```qsharp
operation MultiplexPauli (coefficients : Double[], pauli : Pauli, control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="bc854-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="bc854-106">Description</span></span>

<span data-ttu-id="bc854-107">Hiermee wordt een unitary-bewerking met vermenigvuldiging toegepast waarmee rotaties worden uitgevoerd op basis van hoek $ \ theta_j $ over een Qubit Pauli-operator $P $ wanneer deze wordt beheerd door de $n $-Qubit nummer status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="bc854-107">This applies a multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $P$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="bc854-108">Met name de actie van deze bewerking wordt vertegenwoordigd door de unitary</span><span class="sxs-lookup"><span data-stu-id="bc854-108">In particular, the action of this operation is represented by the unitary</span></span>

<span data-ttu-id="bc854-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i P \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="bc854-109">$$ \begin{align} U = \sum^{2^n - 1}_{j=0} \ket{j}\bra{j} \otimes e^{i P \theta_j}.</span></span>
<span data-ttu-id="bc854-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="bc854-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="bc854-111">Invoer</span><span class="sxs-lookup"><span data-stu-id="bc854-111">Input</span></span>

### <a name="coefficients--double"></a><span data-ttu-id="bc854-112">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="bc854-112">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="bc854-113">Matrix van Maxi maal $2 ^ n $ coëfficiënten $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="bc854-113">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="bc854-114">De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="bc854-114">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="pauli--pauli"></a><span data-ttu-id="bc854-115">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="bc854-115">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="bc854-116">Pauli-operator $P $ die de rotatieas bepaalt.</span><span class="sxs-lookup"><span data-stu-id="bc854-116">Pauli operator $P$ that determines axis of rotation.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="bc854-117">besturings element: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="bc854-117">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="bc854-118">$n $-Qubit-controle register dat nummer Staten $ \ket{j} $ codeert in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="bc854-118">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="bc854-119">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="bc854-119">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="bc854-120">Een single Qubit-REGI ster dat wordt geroteerd door $e ^ {i P \ theta_j} $.</span><span class="sxs-lookup"><span data-stu-id="bc854-120">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bc854-121">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bc854-121">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="bc854-122">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="bc854-122">Remarks</span></span>

<span data-ttu-id="bc854-123">`coefficients` wordt aangevuld met elementen $ \ theta_j = $0,0 als er minder dan $2 ^ n $ is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="bc854-123">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc854-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="bc854-124">See Also</span></span>

- [<span data-ttu-id="bc854-125">Micro soft. Quantum. Canon. ApproximatelyMultiplexPauli</span><span class="sxs-lookup"><span data-stu-id="bc854-125">Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli</span></span>](xref:Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli)