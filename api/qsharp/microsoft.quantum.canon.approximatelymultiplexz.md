---
uid: Microsoft.Quantum.Canon.ApproximatelyMultiplexZ
title: Bewerking ApproximatelyMultiplexZ
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyMultiplexZ
qsharp.summary: Applies a Pauli Z rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: b69b4de62241a7d16c2f07449115f864defda45d
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841095"
---
# <a name="approximatelymultiplexz-operation"></a><span data-ttu-id="30432-102">Bewerking ApproximatelyMultiplexZ</span><span class="sxs-lookup"><span data-stu-id="30432-102">ApproximatelyMultiplexZ operation</span></span>

<span data-ttu-id="30432-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="30432-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="30432-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="30432-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="30432-105">Hiermee wordt een Pauli Z-rotatie toegepast op een matrix van qubits, waarbij kleine rotatie hoeken worden afgekapt volgens een gegeven tolerantie.</span><span class="sxs-lookup"><span data-stu-id="30432-105">Applies a Pauli Z rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.</span></span>

```qsharp
operation ApproximatelyMultiplexZ (tolerance : Double, coefficients : Double[], control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="30432-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="30432-106">Description</span></span>

<span data-ttu-id="30432-107">Hiermee wordt de unitary-bewerking met vermenigvuldiging toegepast waarmee rotaties worden uitgevoerd op basis van hoek $ \ theta_j $ over een Qubit Pauli-operator $Z $, wanneer deze wordt beheerd door de $n $-Qubit nummer status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="30432-107">This applies the multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $Z$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="30432-108">Met name deze bewerking kan worden weer gegeven door de unitary</span><span class="sxs-lookup"><span data-stu-id="30432-108">In particular, this operation can be represented by the unitary</span></span>

<span data-ttu-id="30432-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i Z \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="30432-109">$$ \begin{align} U = \sum^{2^n-1}_{j=0} \ket{j}\bra{j} \otimes e^{i Z \theta_j}.</span></span>
<span data-ttu-id="30432-110">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="30432-110">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="30432-111">Invoer</span><span class="sxs-lookup"><span data-stu-id="30432-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="30432-112">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="30432-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="30432-113">Een tolerantie waaronder kleine coëfficiënten worden afgekapt.</span><span class="sxs-lookup"><span data-stu-id="30432-113">A tolerance below which small coefficients are truncated.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="30432-114">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="30432-114">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="30432-115">Matrix van Maxi maal $2 ^ n $ coëfficiënten $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="30432-115">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="30432-116">De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="30432-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="30432-117">besturings element: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="30432-117">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="30432-118">$n $-Qubit-controle register dat nummer Staten $ \ket{j} $ codeert in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="30432-118">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="30432-119">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="30432-119">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="30432-120">Een single Qubit-REGI ster dat wordt geroteerd door $e ^ {i P \ theta_j} $.</span><span class="sxs-lookup"><span data-stu-id="30432-120">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="30432-121">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="30432-121">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="30432-122">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="30432-122">Remarks</span></span>

<span data-ttu-id="30432-123">`coefficients` wordt aangevuld met elementen $ \ theta_j = $0,0 als er minder dan $2 ^ n $ is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="30432-123">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="references"></a><span data-ttu-id="30432-124">Verwijzingen</span><span class="sxs-lookup"><span data-stu-id="30432-124">References</span></span>

- <span data-ttu-id="30432-125">Synthese van Quantum Logic-circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span><span class="sxs-lookup"><span data-stu-id="30432-125">Synthesis of Quantum Logic Circuits Vivek V. Shende, Stephen S. Bullock, Igor L. Markov https://arxiv.org/abs/quant-ph/0406176</span></span>

## <a name="see-also"></a><span data-ttu-id="30432-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="30432-126">See Also</span></span>

- [<span data-ttu-id="30432-127">Micro soft. Quantum. Canon. MultiplexZ</span><span class="sxs-lookup"><span data-stu-id="30432-127">Microsoft.Quantum.Canon.MultiplexZ</span></span>](xref:Microsoft.Quantum.Canon.MultiplexZ)