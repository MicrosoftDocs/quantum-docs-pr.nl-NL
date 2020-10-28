---
uid: Microsoft.Quantum.Intrinsic.Exp
title: EXP-bewerking
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Exp
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator.

  \begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: b923374a954f90aba2deaead79dd419fbf67fea3
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702134"
---
# <a name="exp-operation"></a><span data-ttu-id="fe85b-102">EXP-bewerking</span><span class="sxs-lookup"><span data-stu-id="fe85b-102">Exp operation</span></span>

<span data-ttu-id="fe85b-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="fe85b-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="fe85b-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fe85b-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fe85b-105">Past de exponentiële waarde van een multi-Qubit Pauli-operator toe.</span><span class="sxs-lookup"><span data-stu-id="fe85b-105">Applies the exponential of a multi-qubit Pauli operator.</span></span>

<span data-ttu-id="fe85b-106">\begin{align} e ^ {i \theta [P_0 \otimes P_1 \cdots P_ {N-1}]}, \end{align} waarbij $P _i $ het $i $ TH element van is `paulis` en waar $N = $ `Length(paulis)` .</span><span class="sxs-lookup"><span data-stu-id="fe85b-106">\begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.</span></span>

```qsharp
operation Exp (paulis : Pauli[], theta : Double, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="fe85b-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="fe85b-107">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="fe85b-108">PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="fe85b-108">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="fe85b-109">Matrix van Pauli-waarden met één Qubit die de tensor-product factoren op elke qubit aangeven.</span><span class="sxs-lookup"><span data-stu-id="fe85b-109">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="theta--double"></a><span data-ttu-id="fe85b-110">Theta: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="fe85b-110">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="fe85b-111">Hoek over de opgegeven multi-Qubit Pauli-operator waarmee het doel register moet worden gedraaid.</span><span class="sxs-lookup"><span data-stu-id="fe85b-111">Angle about the given multi-qubit Pauli operator by which the target register is to be rotated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="fe85b-112">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fe85b-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="fe85b-113">Meld u aan om de gegeven draaiing toe te passen op.</span><span class="sxs-lookup"><span data-stu-id="fe85b-113">Register to apply the given rotation to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fe85b-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fe85b-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

