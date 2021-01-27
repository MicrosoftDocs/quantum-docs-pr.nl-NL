---
uid: Microsoft.Quantum.Canon.ApplyToFirstTwoQubitsCA
title: Bewerking ApplyToFirstTwoQubitsCA
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Canon
qsharp.name: ApplyToFirstTwoQubitsCA
qsharp.summary: Applies an operation to the first two qubits in the register. The modifier `CA` indicates that the operation is controllable and adjointable.
ms.openlocfilehash: 5bea9ec1be1fc379823877684c81e99f86807d89
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98850667"
---
# <a name="applytofirsttwoqubitsca-operation"></a><span data-ttu-id="062ad-102">Bewerking ApplyToFirstTwoQubitsCA</span><span class="sxs-lookup"><span data-stu-id="062ad-102">ApplyToFirstTwoQubitsCA operation</span></span>

<span data-ttu-id="062ad-103">Naam ruimte: [micro soft. Quantum. Canon](xref:Microsoft.Quantum.Canon)</span><span class="sxs-lookup"><span data-stu-id="062ad-103">Namespace: [Microsoft.Quantum.Canon](xref:Microsoft.Quantum.Canon)</span></span>

<span data-ttu-id="062ad-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="062ad-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="062ad-105">Hiermee wordt een bewerking toegepast op de eerste twee qubits in het REGI ster.</span><span class="sxs-lookup"><span data-stu-id="062ad-105">Applies an operation to the first two qubits in the register.</span></span>
<span data-ttu-id="062ad-106">De aanpassings functie `CA` geeft aan dat de bewerking kan worden bestuurd en adjointable.</span><span class="sxs-lookup"><span data-stu-id="062ad-106">The modifier `CA` indicates that the operation is controllable and adjointable.</span></span>

```qsharp
operation ApplyToFirstTwoQubitsCA (op : ((Qubit, Qubit) => Unit is Adj + Ctl), register : Qubit[]) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="062ad-107">Invoer</span><span class="sxs-lookup"><span data-stu-id="062ad-107">Input</span></span>

### <a name="op--qubitqubit--unit--is-adj--ctl"></a><span data-ttu-id="062ad-108">op: ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [eenheid](xref:microsoft.quantum.lang-ref.unit)  is ADJ + CTL</span><span class="sxs-lookup"><span data-stu-id="062ad-108">op : ([Qubit](xref:microsoft.quantum.lang-ref.qubit),[Qubit](xref:microsoft.quantum.lang-ref.qubit)) => [Unit](xref:microsoft.quantum.lang-ref.unit)  is Adj + Ctl</span></span>

<span data-ttu-id="062ad-109">Een bewerking die moet worden toegepast op de eerste twee qubits</span><span class="sxs-lookup"><span data-stu-id="062ad-109">An operation to be applied to the first two qubits</span></span>


### <a name="register--qubit"></a><span data-ttu-id="062ad-110">registreren: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="062ad-110">register : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="062ad-111">Qubit-matrix naar de eerste twee qubits waarop de bewerking wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="062ad-111">Qubit array to the first two qubits of which the operation is applied.</span></span>



## <a name="output--unit"></a><span data-ttu-id="062ad-112">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="062ad-112">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="062ad-113">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="062ad-113">Remarks</span></span>

<span data-ttu-id="062ad-114">Dit komt overeen met:</span><span class="sxs-lookup"><span data-stu-id="062ad-114">This is equivalent to:</span></span>

```qsharp
op(register[0], register[1]);
```

## <a name="see-also"></a><span data-ttu-id="062ad-115">Zie ook</span><span class="sxs-lookup"><span data-stu-id="062ad-115">See Also</span></span>

- [<span data-ttu-id="062ad-116">Micro soft. Quantum. Canon. ApplyToFirstTwoQubits</span><span class="sxs-lookup"><span data-stu-id="062ad-116">Microsoft.Quantum.Canon.ApplyToFirstTwoQubits</span></span>](xref:Microsoft.Quantum.Canon.ApplyToFirstTwoQubits)