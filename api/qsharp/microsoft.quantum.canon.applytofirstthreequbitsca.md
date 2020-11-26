---
uid: Microsoft.Quantum.Canon.ApplyToFirstThreeQubitsCA
title: Bewerking ApplyToFirstThreeQubitsCA
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstThreeQubitsCA
qsharp.summary: Applies an operation to the first three qubits in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 7e090a116a63e26278b05dc7c2fda9b65ff15bae
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96208785"
---
# <a name="applytofirstthreequbitsca-operation"></a><span data-ttu-id="26f4d-102">Bewerking ApplyToFirstThreeQubitsCA</span><span class="sxs-lookup"><span data-stu-id="26f4d-102">ApplyToFirstThreeQubitsCA operation</span></span>

<span data-ttu-id="26f4d-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="26f4d-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="26f4d-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="26f4d-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="26f4d-105">Hiermee wordt een bewerking toegepast op de eerste drie qubits in het REGI ster.</span><span class="sxs-lookup"><span data-stu-id="26f4d-105">Applies an operation to the first three qubits in the register.</span></span>
<span data-ttu-id="26f4d-106">De aanpassings functie `CA` geeft aan dat de bewerking kan worden bestuurd en adjointable.</span><span class="sxs-lookup"><span data-stu-id="26f4d-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToFirstThreeQubitsCA (op : ((Qubit, Qubit, Qubit) => Unit is Adj + Ctl), register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="26f4d-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="26f4d-107">Input</span></span>

### <a name="op--qubitqubitqubit--unit--is-adj--ctl"></a><span data-ttu-id="26f4d-108">op: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ en CTL</span><span class="sxs-lookup"><span data-stu-id="26f4d-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="26f4d-109">Een bewerking die moet worden toegepast op de eerste drie qubits</span><span class="sxs-lookup"><span data-stu-id="26f4d-109">An operation to be applied to the first three qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="26f4d-110">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="26f4d-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="26f4d-111">Qubit-matrix naar de eerste drie qubits waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="26f4d-111">Qubit array to the first three qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="26f4d-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="26f4d-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="26f4d-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="26f4d-113">Remarks</span></span>

<span data-ttu-id="26f4d-114">Dit komt overeen met:</span><span class="sxs-lookup"><span data-stu-id="26f4d-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1], register[2]);
```

## <a name="see-also"></a><span data-ttu-id="26f4d-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="26f4d-115">See Also</span></span>

- [<span data-ttu-id="26f4d-116">Micro soft. Quantum. Canon. ApplyToFirstThreeQubits</span><span class="sxs-lookup"><span data-stu-id="26f4d-116">Microsoft.Quantum.Canon.ApplyToFirstThreeQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstThreeQubits)