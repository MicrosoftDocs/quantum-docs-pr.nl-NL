---
uid: Microsoft.Quantum.Diagnostics.AssertAllZeroWithinTolerance
title: Bewerking AssertAllZeroWithinTolerance
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AssertAllZeroWithinTolerance
qsharp.summary: Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.
ms.openlocfilehash: 5e401904086323fabef7914d34463f50e4c38862
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702783"
---
# <a name="assertallzerowithintolerance-operation"></a><span data-ttu-id="d0e3d-102">Bewerking AssertAllZeroWithinTolerance</span><span class="sxs-lookup"><span data-stu-id="d0e3d-102">AssertAllZeroWithinTolerance operation</span></span>

<span data-ttu-id="d0e3d-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="d0e3d-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="d0e3d-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d0e3d-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d0e3d-105">De bevestiging dat de opgegeven qubits zich in $ \ket $-status bevindt, {0} tot een gegeven tolerantie.</span><span class="sxs-lookup"><span data-stu-id="d0e3d-105">Assert that given qubits are all in $\ket{0}$ state up to a given tolerance.</span></span>

```qsharp
operation AssertAllZeroWithinTolerance (qubits : Qubit[], tolerance : Double) : Unit
```


## <a name="input"></a><span data-ttu-id="d0e3d-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d0e3d-106">Input</span></span>

### <a name="qubits--qubit"></a><span data-ttu-id="d0e3d-107">qubits: [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span><span class="sxs-lookup"><span data-stu-id="d0e3d-107">qubits : [Qubit](xref:microsoft.quantum.lang-ref.qubit)[]</span></span>

<span data-ttu-id="d0e3d-108">Qubits die zijn bewering over $ \ket $- {0} status.</span><span class="sxs-lookup"><span data-stu-id="d0e3d-108">Qubits that are asserted to be in $\ket{0}$ state.</span></span>


### <a name="tolerance--double"></a><span data-ttu-id="d0e3d-109">tolerantie: [dubbel](xref:microsoft.quantum.lang-ref.double)</span><span class="sxs-lookup"><span data-stu-id="d0e3d-109">tolerance : [Double](xref:microsoft.quantum.lang-ref.double)</span></span>

<span data-ttu-id="d0e3d-110">Nauw keurigheid waarmee de status moet worden in $ \ket {0} $ State</span><span class="sxs-lookup"><span data-stu-id="d0e3d-110">Accuracy with which the state should be in $\ket{0}$ state</span></span>



## <a name="output--unit"></a><span data-ttu-id="d0e3d-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d0e3d-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="see-also"></a><span data-ttu-id="d0e3d-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d0e3d-112">See Also</span></span>

- [<span data-ttu-id="d0e3d-113">Micro soft. Quantum. Diagnostics. AssertQubitWithinTolerance</span><span class="sxs-lookup"><span data-stu-id="d0e3d-113">Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance</span></span>](xref:Microsoft.Quantum.Diagnostics.AssertQubitWithinTolerance)