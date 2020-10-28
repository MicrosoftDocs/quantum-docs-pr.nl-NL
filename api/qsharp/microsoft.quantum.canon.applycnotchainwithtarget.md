---
uid: Microsoft.Quantum.Canon.ApplyCNOTChainWithTarget
title: Bewerking ApplyCNOTChainWithTarget
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyCNOTChainWithTarget
qsharp.summary: Computes the parity of an array of qubits into a target qubit.
ms.openlocfilehash: fd0a0f3e1db89946aec2c63f3cde7a021608eea5
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92705437"
---
# <a name="applycnotchainwithtarget-operation"></a><span data-ttu-id="fbf47-102">Bewerking ApplyCNOTChainWithTarget</span><span class="sxs-lookup"><span data-stu-id="fbf47-102">ApplyCNOTChainWithTarget operation</span></span>

<span data-ttu-id="fbf47-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="fbf47-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="fbf47-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="fbf47-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="fbf47-105">Hiermee wordt de pariteit van een matrix met qubits berekend in een doel-Qubit.</span><span class="sxs-lookup"><span data-stu-id="fbf47-105">Computes the parity of an array of qubits into a target qubit.</span></span>

```qsharp
operation ApplyCNOTChainWithTarget (qubits : Qubit[], targetQubit : Qubit) : Unit
```


## <a name="description"></a><span data-ttu-id="fbf47-106">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="fbf47-106">Description</span></span>

<span data-ttu-id="fbf47-107">Als de matrix in eerste instantie de status $ \ket{q_0} \ket{q_1} \cdots \ket{q_ {\Text{target}}} $ heeft, wordt de uiteindelijke status gegeven door $ \ket{q_0} \ket{q_1 \oplus q_0} \cdots \ket{q_ {n-1} \oplus \cdots \oplus q_0 \oplus q_ {\Text{target}}} $.</span><span class="sxs-lookup"><span data-stu-id="fbf47-107">If the array is initially in the state $\ket{q_0} \ket{q_1} \cdots \ket{q_{\text{target}}}$, the final state is given by $\ket{q_0} \ket{q_1 \oplus q_0} \cdots \ket{q_{n - 1} \oplus \cdots \oplus q_0 \oplus q_{\text{target}}}$.</span></span>

## <a name="input"></a><span data-ttu-id="fbf47-108">Invoer</span><span class="sxs-lookup"><span data-stu-id="fbf47-108">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="fbf47-109">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="fbf47-109">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="fbf47-110">Matrix van qubits waarop de pariteit wordt berekend.</span><span class="sxs-lookup"><span data-stu-id="fbf47-110">Array of qubits on which the parity is computed.</span></span>


### <a name="targetqubit--qubit"></a><span data-ttu-id="fbf47-111">targetQubit: [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span><span class="sxs-lookup"><span data-stu-id="fbf47-111">targetQubit : [Qubit](xref:microsoft.quantum.lang-ref.qubit)</span></span>

<span data-ttu-id="fbf47-112">Eind Qubit waarin de pariteit van qubits is XORed.</span><span class="sxs-lookup"><span data-stu-id="fbf47-112">Final qubit into which the parity of 'qubits' is XORed.</span></span>



## <a name="output--unit"></a><span data-ttu-id="fbf47-113">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="fbf47-113">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="fbf47-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="fbf47-114">Remarks</span></span>

<span data-ttu-id="fbf47-115">De volgende zijn gelijkwaardig:</span><span class="sxs-lookup"><span data-stu-id="fbf47-115">The following are equivalent:</span></span>

```qsharp
ApplyCNOTChainWithTarget(Most(qs), Last(qs));
```

<span data-ttu-id="fbf47-116">en</span><span class="sxs-lookup"><span data-stu-id="fbf47-116">and</span></span>

```qsharp
ApplyCNOTChain(qs);
```