---
uid: Microsoft.Quantum.Diagnostics.AssertAllZeroWithinTolerance
title: Bewerking AssertAllZeroWithinTolerance
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertAllZeroWithinTolerance
qsharp.summary: Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.
ms.openlocfilehash: 281855ec79d280c903ebb4d05614081767840778
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830851"
---
# <a name="assertallzerowithintolerance-operation"></a><span data-ttu-id="86ccf-102">Bewerking AssertAllZeroWithinTolerance</span><span class="sxs-lookup"><span data-stu-id="86ccf-102">AssertAllZeroWithinTolerance operation</span></span>

<span data-ttu-id="86ccf-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="86ccf-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="86ccf-104">Pakket: [micro soft. Quantum. QSharp. core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span><span class="sxs-lookup"><span data-stu-id="86ccf-104">Package: [Microsoft.Quantum.QSharp.Core](https://nuget.org/packages/Microsoft.Quantum.QSharp.Core)</span></span>


<span data-ttu-id="86ccf-105">De bevestiging dat de opgegeven qubits zich in $ \ket $-status bevindt, {0} tot een gegeven tolerantie.</span><span class="sxs-lookup"><span data-stu-id="86ccf-105">Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.</span></span>

```qsharp
operation AssertAllZeroWithinTolerance (qubits : Qubit[], tolerance : Double) : Unit is Adj + Ctl
```


## <a name="input"></a><span data-ttu-id="86ccf-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="86ccf-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="86ccf-107">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="86ccf-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="86ccf-108">Qubits die zijn bewering over $ \ket $- {0} status.</span><span class="sxs-lookup"><span data-stu-id="86ccf-108">Qubits that are asserted to be in $\ket{0}$ state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="86ccf-109">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="86ccf-109">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="86ccf-110">Nauw keurigheid waarmee de status moet worden in $ \ket {0} $ State</span><span class="sxs-lookup"><span data-stu-id="86ccf-110">Accuracy with which the state should be in $\ket{0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="86ccf-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="86ccf-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="86ccf-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="86ccf-112">See Also</span></span>

- [<span data-ttu-id="86ccf-113">Micro soft. Quantum. Diagnostics. AssertQubitWithinTolerance</span><span class="sxs-lookup"><span data-stu-id="86ccf-113">Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance)