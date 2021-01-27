---
uid: Microsoft.Quantum.Intrinsic.ExpFrac
title: Bewerking ExpFrac
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Intrinsic
qsharp.name: ExpFrac
qsharp.summary: >-
  Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.

  \begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.
ms.openlocfilehash: 6634caff164c841876fb53e79c3f93254a7d624c
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98849419"
---
# <a name="expfrac-operation"></a><span data-ttu-id="c3366-102">Bewerking ExpFrac</span><span class="sxs-lookup"><span data-stu-id="c3366-102">ExpFrac operation</span></span>

<span data-ttu-id="c3366-103">Naam ruimte: [micro soft. Quantum. intrinsiek](xref:Microsoft.Quantum.Intrinsic)</span><span class="sxs-lookup"><span data-stu-id="c3366-103">Namespace: [Microsoft.Quantum.Intrinsic](xref:Microsoft.Quantum.Intrinsic)</span></span>

<span data-ttu-id="c3366-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="c3366-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="c3366-105">Past de exponentiële waarde toe van een multi-Qubit Pauli-operator met een argument dat door een dyadic-fractie wordt gegeven.</span><span class="sxs-lookup"><span data-stu-id="c3366-105">Applies the exponential of a multi-qubit Pauli operator with an argument given by a dyadic fraction.</span></span>

<span data-ttu-id="c3366-106">\begin{align} e ^ {i \pi k [P_0 \otimes P_1 \cdots P_ {N-1}]/2 ^ N}, \end{align} waarbij $P _i $ het $i $ TH element van is `paulis` en waar $N = $ `Length(paulis)` .</span><span class="sxs-lookup"><span data-stu-id="c3366-106">\begin{align} e^{i \pi k [P_0 \otimes P_1 \cdots P_{N-1}] / 2^n}, \end{align} where $P_i$ is the $i$th element of `paulis`, and where $N = $`Length(paulis)`.</span></span>

```qsharp
operation ExpFrac (paulis : Pauli[], numerator : Int, power : Int, qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="c3366-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="c3366-107">Input</span></span>

### <a name="paulis--pauli"></a><span data-ttu-id="c3366-108">PAULIS: [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span><span class="sxs-lookup"><span data-stu-id="c3366-108">paulis : [Pauli](xref:microsoft.quantum.lang-ref.pauli)[]</span></span>

<span data-ttu-id="c3366-109">Matrix van Pauli-waarden met één Qubit die de tensor-product factoren op elke qubit aangeven.</span><span class="sxs-lookup"><span data-stu-id="c3366-109">Array of single-qubit Pauli values indicating the tensor product factors on each qubit.</span></span>


### <a name="numerator--int"></a><span data-ttu-id="c3366-110">teller: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c3366-110">numerator : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c3366-111">Teller ($k $) in de dyadic-weer gave van de hoek waarmee het Qubit-REGI ster moet worden gedraaid.</span><span class="sxs-lookup"><span data-stu-id="c3366-111">Numerator ($k$) in the dyadic fraction representation of the angle by which the qubit register is to be rotated.</span></span>


### <a name="power--int"></a><span data-ttu-id="c3366-112">energie: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="c3366-112">power : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="c3366-113">Kracht van twee ($n $) waarmee de noemer wordt aangegeven van de hoek waarmee het Qubit-REGI ster moet worden gedraaid.</span><span class="sxs-lookup"><span data-stu-id="c3366-113">Power of two ($n$) specifying the denominator of the angle by which the qubit register is to be rotated.</span></span>


### <a name="qubits--qubit"></a><span data-ttu-id="c3366-114">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="c3366-114">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="c3366-115">Meld u aan om de gegeven draaiing toe te passen op.</span><span class="sxs-lookup"><span data-stu-id="c3366-115">Register to apply the given rotation to.</span></span>



## <a name="output--unit"></a><span data-ttu-id="c3366-116">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="c3366-116">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

