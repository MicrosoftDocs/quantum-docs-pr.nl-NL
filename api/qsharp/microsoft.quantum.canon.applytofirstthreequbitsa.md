---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsA
title: Bewerking ApplyToFirstThreeQubitsA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsA
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `A` indicates that the operation is adjointable.
ms.openlocfilehash: c3374ceba9f442f9315d4b5fc54b158327124926
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208768"
---
# <a name="applytofirstthreequbitsa-operation"></a><span data-ttu-id="a29ee-102">Bewerking ApplyToFirstThreeQubitsA</span><span class="sxs-lookup"><span data-stu-id="a29ee-102">ApplyToFirstThreeQubitsA operation</span></span>

<span data-ttu-id="a29ee-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="a29ee-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="a29ee-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="a29ee-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="a29ee-105">Hiermee wordt een bewerking toegepast op de eerste drie qubits in het REGI ster.</span><span class="sxs-lookup"><span data-stu-id="a29ee-105">Applies an operation to the first three qubits in the register.</span></span>
<span data-ttu-id="a29ee-106">De aanpassings functie `A` geeft aan dat de bewerking is adjointable.</span><span class="sxs-lookup"><span data-stu-id="a29ee-106">The modifier `A` indicates that the operation is adjointable.</span></span>

```qsharp
operation ApplyToFirstThreeQubitsA (op : ((Qubit, Qubit, Qubit) => Unit is Adj), register : Qubit[]) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="a29ee-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="a29ee-107">Input</span></span>

### <a name="op--qubitqubitqubit--unit--is-adj"></a><span data-ttu-id="a29ee-108">op: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ</span><span class="sxs-lookup"><span data-stu-id="a29ee-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj</span></span>

<span data-ttu-id="a29ee-109">Een bewerking die moet worden toegepast op de eerste drie qubits</span><span class="sxs-lookup"><span data-stu-id="a29ee-109">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="a29ee-110">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="a29ee-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="a29ee-111">Qubit-matrix naar de eerste drie qubits waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="a29ee-111">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="a29ee-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="a29ee-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="a29ee-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="a29ee-113">Remarks</span></span>

<span data-ttu-id="a29ee-114">Dit komt overeen met:</span><span class="sxs-lookup"><span data-stu-id="a29ee-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="a29ee-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a29ee-115">See Also</span></span>

- [<span data-ttu-id="a29ee-116">Micro soft. Quantum. Canon. ApplyToFirstThreeQubits</span><span class="sxs-lookup"><span data-stu-id="a29ee-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubits)