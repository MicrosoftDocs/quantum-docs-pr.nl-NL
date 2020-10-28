---
uid: Microsoft.Quantum.Intrinsic.ExpFrac
title: Bewerking ExpFrac
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ExpFrac
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.

  \begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: d11912a272387b087098f59e7ac071534b01c054
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702117"
---
# <a name="expfrac-operation"></a><span data-ttu-id="bc4d1-102">Bewerking ExpFrac</span><span class="sxs-lookup"><span data-stu-id="bc4d1-102">ExpFrac operation</span></span>

<span data-ttu-id="bc4d1-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="bc4d1-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="bc4d1-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="bc4d1-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="bc4d1-105">Past de exponentiële waarde toe van een multi-Qubit Pauli-operator met een argument dat door een dyadic-fractie wordt gegeven.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-105">Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.</span></span>

<span data-ttu-id="bc4d1-106">\begin{align} e ^ {i \pi k [P_0 \otimes P_1 \cdots P_ {N-1}]/2 ^ N}, \end{align} waarbij $P _i $ het $i $ TH element van is `paulis` en waar $N = $ `Length(paulis)` .</span><span class="sxs-lookup"><span data-stu-id="bc4d1-106">\begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.</span></span>

```qsharp
operation ExpFrac (paulis : Pauli[], numerator : Int, power : Int, qubits : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="bc4d1-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="bc4d1-107">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="bc4d1-108">PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="bc4d1-108">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="bc4d1-109">Matrix van Pauli-waarden met één Qubit die de tensor-product factoren op elke qubit aangeven.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-109">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="numerator--int"></a><span data-ttu-id="bc4d1-110">teller: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bc4d1-110">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bc4d1-111">Teller ($k $) in de dyadic-weer gave van de hoek waarmee het Qubit-REGI ster moet worden gedraaid.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-111">Numerator ($k$) in the dyadic fraction representation of the angle by which the qubit register is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="bc4d1-112">energie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="bc4d1-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="bc4d1-113">Kracht van twee ($n $) waarmee de noemer wordt aangegeven van de hoek waarmee het Qubit-REGI ster moet worden gedraaid.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-113">Power of two ($n$) specifying the denominator of the angle by which the qubit register is to be rotated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="bc4d1-114">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="bc4d1-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="bc4d1-115">Meld u aan om de gegeven draaiing toe te passen op.</span><span class="sxs-lookup"><span data-stu-id="bc4d1-115">Register to apply the given rotation to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="bc4d1-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="bc4d1-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

