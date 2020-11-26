---
uid: Microsoft.Quantum.Canon.ApproximatelyMultiplexPauli
title: Bewerking ApproximatelyMultiplexPauli
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApproximatelyMultiplexPauli
qsharp.summary: Applies a Pauli rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.
ms.openlocfilehash: 8024df4608f14408bfcd46139e72454ff44b116f
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96207748"
---
# <a name="approximatelymultiplexpauli-operation"></a><span data-ttu-id="ca6b9-102">Bewerking ApproximatelyMultiplexPauli</span><span class="sxs-lookup"><span data-stu-id="ca6b9-102">ApproximatelyMultiplexPauli operation</span></span>

<span data-ttu-id="ca6b9-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="ca6b9-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="ca6b9-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="ca6b9-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="ca6b9-105">Hiermee wordt een Pauli-rotatie toegepast op een matrix van qubits, waarbij kleine rotatie hoeken worden afgekapt volgens een gegeven tolerantie.</span><span class="sxs-lookup"><span data-stu-id="ca6b9-105">Applies a Pauli rotation conditioned on an array of qubits, truncating small rotation angles according to a given tolerance.</span></span>

```qsharp
operation ApproximatelyMultiplexPauli (tolerance : Double, coefficients : Double[], pauli : Pauli, control : Microsoft.Quantum.Arithmetic.LittleEndian, target : Qubit) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="ca6b9-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ca6b9-106">Description</span></span>

<span data-ttu-id="ca6b9-107">Hiermee wordt een unitary-bewerking met vermenigvuldiging toegepast waarmee rotaties worden uitgevoerd op basis van hoek $ \ theta_j $ over een Qubit Pauli-operator $P $ wanneer deze wordt beheerd door de $n $-Qubit nummer status $ \ket{j} $.</span><span class="sxs-lookup"><span data-stu-id="ca6b9-107">This applies a multiply controlled unitary operation that performs rotations by angle $\theta_j$ about single-qubit Pauli operator $P$ when controlled by the $n$-qubit number state $\ket{j}$.</span></span>
<span data-ttu-id="ca6b9-108">Met name de actie van deze bewerking wordt vertegenwoordigd door de unitary</span><span class="sxs-lookup"><span data-stu-id="ca6b9-108">In particular, the action of this operation is represented by the unitary</span></span>

<span data-ttu-id="ca6b9-109">$ $ \begin{align} U = \sum ^ {2 ^ n-1} _ {j = 0} \ket{j}\bra{j} \otimes e ^ {i P \ theta_j}.</span><span class="sxs-lookup"><span data-stu-id="ca6b9-109">$$ \begin{align} U = \sum^{2^n - 1}_{j=0} \ket{j}\bra{j} \otimes e^{i P \theta_j}.</span></span>
<span data-ttu-id="ca6b9-110">\end{align}</span><span class="sxs-lookup"><span data-stu-id="ca6b9-110">\end{align}</span></span>

##

## <a name="input"></a><span data-ttu-id="ca6b9-111">Invoer</span><span class="sxs-lookup"><span data-stu-id="ca6b9-111">Input</span></span>

### <a name="tolerance--double"></a><span data-ttu-id="ca6b9-112">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="ca6b9-112">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="ca6b9-113">Een tolerantie waaronder kleine coëfficiënten worden afgekapt.</span><span class="sxs-lookup"><span data-stu-id="ca6b9-113">A tolerance below which small coefficients are truncated.</span></span>


### <a name="coefficients--double"></a><span data-ttu-id="ca6b9-114">coëfficiënten: [dubbel](xref:microsoft.quantum.lang-ref.double)[]</span><span class="sxs-lookup"><span data-stu-id="ca6b9-114">coefficients : [Double](xref:microsoft.quantum.lang-ref.double)[]</span></span>

<span data-ttu-id="ca6b9-115">Matrix van Maxi maal $2 ^ n $ coëfficiënten $ \ theta_j $.</span><span class="sxs-lookup"><span data-stu-id="ca6b9-115">Array of up to $2^n$ coefficients $\theta_j$.</span></span> <span data-ttu-id="ca6b9-116">De $j $ th indexeert de nummer status $ \ket{j} $ gecodeerd in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="ca6b9-116">The $j$th coefficient indexes the number state $\ket{j}$ encoded in little-endian format.</span></span>


### <a name="pauli--pauli"></a><span data-ttu-id="ca6b9-117">Pauli: [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span><span class="sxs-lookup"><span data-stu-id="ca6b9-117">pauli : [Pauli](xref:microsoft.quantum.lang-ref.pauli)</span></span>

<span data-ttu-id="ca6b9-118">Pauli-operator $P $ die de rotatieas bepaalt.</span><span class="sxs-lookup"><span data-stu-id="ca6b9-118">Pauli operator $P$ that determines axis of rotation.</span></span>


### <a name="control--littleendian"></a><span data-ttu-id="ca6b9-119">besturings element: [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span><span class="sxs-lookup"><span data-stu-id="ca6b9-119">control : [LittleEndian](xref:Microsoft.Quantum.Arithmetic.LittleEndian)</span></span>

<span data-ttu-id="ca6b9-120">$n $-Qubit-controle register dat nummer Staten $ \ket{j} $ codeert in de indeling little endian.</span><span class="sxs-lookup"><span data-stu-id="ca6b9-120">$n$-qubit control register that encodes number states $\ket{j}$ in little-endian format.</span></span>


### <a name="target--qubit"></a><span data-ttu-id="ca6b9-121">doel: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="ca6b9-121">target : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="ca6b9-122">Een single Qubit-REGI ster dat wordt geroteerd door $e ^ {i P \ theta_j} $.</span><span class="sxs-lookup"><span data-stu-id="ca6b9-122">Single qubit register that is rotated by $e^{i P \theta_j}$.</span></span>



## <a name="output--unit"></a><span data-ttu-id="ca6b9-123">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="ca6b9-123">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="ca6b9-124">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="ca6b9-124">Remarks</span></span>

<span data-ttu-id="ca6b9-125">`coefficients` wordt aangevuld met elementen $ \ theta_j = $0,0 als er minder dan $2 ^ n $ is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="ca6b9-125">`coefficients` will be padded with elements $\theta_j = 0.0$ if fewer than $2^n$ are specified.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca6b9-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ca6b9-126">See Also</span></span>

- [<span data-ttu-id="ca6b9-127">Micro soft. Quantum. Canon. MultiplexPauli</span><span class="sxs-lookup"><span data-stu-id="ca6b9-127">Microsoft.Quantum.Canon.MultiplexPauli</span></span>](xref:Microsoft.Quantum.Canon.MultiplexPauli)