---
uid: Microsoft.Quantum.Canon.ApplyCNOTChain
title: Bewerking ApplyCNOTChain
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChain
qsharp.summary: Computes the parity of a register of qubits in-place.
ms.openlocfilehash: e237e4424661de816e73b0c78523180b41190cf9
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96219138"
---
# <a name="applycnotchain-operation"></a><span data-ttu-id="9ab6d-102">Bewerking ApplyCNOTChain</span><span class="sxs-lookup"><span data-stu-id="9ab6d-102">ApplyCNOTChain operation</span></span>

<span data-ttu-id="9ab6d-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="9ab6d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="9ab6d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="9ab6d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="9ab6d-105">Hiermee wordt de pariteit van een REGI ster van qubits in-place berekend.</span><span class="sxs-lookup"><span data-stu-id="9ab6d-105">Computes the parity of a register of qubits in-place.</span></span>

```qsharp
operation ApplyCNOTChain (qubits : Qubit[]) : Unit is Adj + Ctl
```


## <a name="description"></a><span data-ttu-id="9ab6d-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="9ab6d-106">Description</span></span>

<span data-ttu-id="9ab6d-107">Met deze bewerking wordt de status van de invoer getransformeerd als $ $ \begin{align} \ket{q_0} \ket{q_1} \cdots \ket{q_ {n-1}} & \mapsto \ket{q_0} \ket{q_0 \oplus q_1} \ket{q_0 \oplus q_1 \oplus q_2} \cdots \ket{q_0 \oplus \cdots \oplus q_ {n-1}}.</span><span class="sxs-lookup"><span data-stu-id="9ab6d-107">This operation transforms the state of its input as $$ \begin{align} \ket{q_0} \ket{q_1} \cdots \ket{q_{n - 1}} & \mapsto \ket{q_0} \ket{q_0 \oplus q_1} \ket{q_0 \oplus q_1 \oplus q_2} \cdots \ket{q_0 \oplus \cdots \oplus q_{n - 1}}.</span></span>
<span data-ttu-id="9ab6d-108">\end{align} $ $</span><span class="sxs-lookup"><span data-stu-id="9ab6d-108">\end{align} $$</span></span>

## <a name="input"></a><span data-ttu-id="9ab6d-109">Invoer</span><span class="sxs-lookup"><span data-stu-id="9ab6d-109">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="9ab6d-110">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="9ab6d-110">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="9ab6d-111">Matrix van qubits waarvan de pariteit moet worden berekend en opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="9ab6d-111">Array of qubits whose parity is to be computed and stored.</span></span>



## <a name="output--unit"></a><span data-ttu-id="9ab6d-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="9ab6d-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>

