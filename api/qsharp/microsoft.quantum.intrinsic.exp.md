---
uid: Microsoft.Quantum.Intrinsic.Exp
title: EXP-bewerking
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: Exp
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator.

  \begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: 7aa6974e83e917125b63ef91fb5c3b1238f6e856
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98819013"
---
# <a name="exp-operation"></a><span data-ttu-id="54698-102">EXP-bewerking</span><span class="sxs-lookup"><span data-stu-id="54698-102">Exp operation</span></span>

<span data-ttu-id="54698-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="54698-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="54698-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="54698-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="54698-105">Past de exponentiële waarde van een multi-Qubit Pauli-operator toe.</span><span class="sxs-lookup"><span data-stu-id="54698-105">Applies the exponential of a multi-qubit Pauli operator.</span></span>

<span data-ttu-id="54698-106">\begin{align} e ^ {i \theta [P_0 \otimes P_1 \cdots P_ {N-1}]}, \end{align} waarbij $P _i $ het $i $ TH element van is `paulis` en waar $N = $ `Length(paulis)` .</span><span class="sxs-lookup"><span data-stu-id="54698-106">\begin{align} e^{i \theta [P_0 \otimes P_1 \cdots P_{N-1}]}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.</span></span>

```qsharp
operation Exp (paulis : Pauli[], theta : Double, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="54698-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="54698-107">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="54698-108">PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="54698-108">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="54698-109">Matrix van Pauli-waarden met één Qubit die de tensor-product factoren op elke qubit aangeven.</span><span class="sxs-lookup"><span data-stu-id="54698-109">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="theta--double"></a><span data-ttu-id="54698-110">Theta: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="54698-110">theta : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="54698-111">Hoek over de opgegeven multi-Qubit Pauli-operator waarmee het doel register moet worden gedraaid.</span><span class="sxs-lookup"><span data-stu-id="54698-111">Angle about the given multi-qubit Pauli operator by which the target register is to be rotated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="54698-112">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="54698-112">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="54698-113">Meld u aan om de gegeven draaiing toe te passen op.</span><span class="sxs-lookup"><span data-stu-id="54698-113">Register to apply the given rotation to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="54698-114">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="54698-114">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

