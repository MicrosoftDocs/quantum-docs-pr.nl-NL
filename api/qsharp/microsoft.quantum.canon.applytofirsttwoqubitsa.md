---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA
title: Bewerking ApplyToFirstTwoQubitsA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsA
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: 1a286c167a87372dc89d62ab3733b186298c43a1
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208700"
---
# <a name="applytofirsttwoqubitsa-operation"></a><span data-ttu-id="280ad-102">Bewerking ApplyToFirstTwoQubitsA</span><span class="sxs-lookup"><span data-stu-id="280ad-102">ApplyToFirstTwoQubitsA operation</span></span>

<span data-ttu-id="280ad-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="280ad-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="280ad-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="280ad-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="280ad-105">Hiermee wordt een bewerking toegepast op de eerste twee qubits in het REGI ster.</span><span class="sxs-lookup"><span data-stu-id="280ad-105">Applies an operation to the first two qubits in the register.</span></span>
<span data-ttu-id="280ad-106">De aanpassings functie `A` geeft aan dat de bewerking is adjointable.</span><span class="sxs-lookup"><span data-stu-id="280ad-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstTwoQubitsA (op : ((Qubit, Qubit) => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="280ad-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="280ad-107">Input</span></span>

### <a name="op--qubitqubit--unit--is-adj"></a><span data-ttu-id="280ad-108">op: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is correctie</span><span class="sxs-lookup"><span data-stu-id="280ad-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="280ad-109">Een bewerking die moet worden toegepast op de eerste twee qubits</span><span class="sxs-lookup"><span data-stu-id="280ad-109">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="280ad-110">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="280ad-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="280ad-111">Qubit-matrix naar de eerste twee qubits waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="280ad-111">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="280ad-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="280ad-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="280ad-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="280ad-113">Remarks</span></span>

<span data-ttu-id="280ad-114">Dit komt overeen met:</span><span class="sxs-lookup"><span data-stu-id="280ad-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="280ad-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="280ad-115">See Also</span></span>

- [<span data-ttu-id="280ad-116">Micro soft. Quantum. Canon. ApplyToFirstTwoQubits</span><span class="sxs-lookup"><span data-stu-id="280ad-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)