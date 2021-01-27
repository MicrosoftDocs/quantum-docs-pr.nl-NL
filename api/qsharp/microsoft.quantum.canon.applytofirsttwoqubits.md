---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubits
title: Bewerking ApplyToFirstTwoQubits
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubits
qsharp.summary: Applies an operation to the first two qubits in the register.
ms.openlocfilehash: c89ea89c055a950a9aee533653d40c84d8e179da
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98841368"
---
# <a name="applytofirsttwoqubits-operation"></a><span data-ttu-id="be1d5-102">Bewerking ApplyToFirstTwoQubits</span><span class="sxs-lookup"><span data-stu-id="be1d5-102">ApplyToFirstTwoQubits operation</span></span>

<span data-ttu-id="be1d5-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="be1d5-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="be1d5-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="be1d5-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="be1d5-105">Hiermee wordt een bewerking toegepast op de eerste twee qubits in het REGI ster.</span><span class="sxs-lookup"><span data-stu-id="be1d5-105">Applies an operation to the first two qubits in the register.</span></span>

```qsharp
operation ApplyToFirstTwoQubits (op : ((Qubit, Qubit) => Unit), register : Qubit[]) : Unit
```


## <a name="input"></a><span data-ttu-id="be1d5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="be1d5-106">Input</span></span>

### <a name="op--qubitqubit--unit"></a><span data-ttu-id="be1d5-107">op: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="be1d5-107">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span> 

<span data-ttu-id="be1d5-108">Een bewerking die moet worden toegepast op de eerste twee qubits</span><span class="sxs-lookup"><span data-stu-id="be1d5-108">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="be1d5-109">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="be1d5-109">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="be1d5-110">Qubit-matrix naar de eerste twee qubits waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="be1d5-110">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="be1d5-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="be1d5-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="be1d5-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="be1d5-112">Remarks</span></span>

<span data-ttu-id="be1d5-113">Dit komt overeen met:</span><span class="sxs-lookup"><span data-stu-id="be1d5-113">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="be1d5-114">Zie ook</span><span class="sxs-lookup"><span data-stu-id="be1d5-114">See Also</span></span>

- [<span data-ttu-id="be1d5-115">Micro soft. Quantum. Canon. ApplyToFirstTwoQubitsA</span><span class="sxs-lookup"><span data-stu-id="be1d5-115">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsA)
- [<span data-ttu-id="be1d5-116">Micro soft. Quantum. Canon. ApplyToFirstTwoQubitsC</span><span class="sxs-lookup"><span data-stu-id="be1d5-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsC)
- [<span data-ttu-id="be1d5-117">Micro soft. Quantum. Canon. ApplyToFirstTwoQubitsCA</span><span class="sxs-lookup"><span data-stu-id="be1d5-117">Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA)