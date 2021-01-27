---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNQubits
title: Bewerking AllowAtMostNQubits
ms.date: 1/23/2021 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNQubits
qsharp.summary: Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.
ms.openlocfilehash: 3aa80767ac0f752e7be0efa2966c580ca3cb8f19
ms.sourcegitcommit: 71605ea9cc630e84e7ef29027e1f0ea06299747e
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/26/2021
ms.locfileid: "98830915"
---
# <a name="allowatmostnqubits-operation"></a><span data-ttu-id="40b72-102">Bewerking AllowAtMostNQubits</span><span class="sxs-lookup"><span data-stu-id="40b72-102">AllowAtMostNQubits operation</span></span>

<span data-ttu-id="40b72-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="40b72-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="40b72-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="40b72-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="40b72-105">Tussen een aanroep van deze bewerking en de adjoint, wordt met behulp van-instructies gecontroleerd of er Maxi maal een gegeven aantal extra qubits is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="40b72-105">Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.</span></span>

```qsharp
operation AllowAtMostNQubits (nQubits : Int, message : String) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="40b72-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="40b72-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="40b72-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="40b72-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="40b72-108">Het maximum aantal qubits dat kan worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="40b72-108">The maximum number of qubits that may be allocated.</span></span>


### <a name="message--string"></a><span data-ttu-id="40b72-109">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="40b72-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="40b72-110">Een bericht dat wordt weer gegeven wanneer de fout is opgetreden.</span><span class="sxs-lookup"><span data-stu-id="40b72-110">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="40b72-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="40b72-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="example"></a><span data-ttu-id="40b72-112">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="40b72-112">Example</span></span>

<span data-ttu-id="40b72-113">Het volgende code fragment mislukt wanneer dit wordt uitgevoerd op machines die deze diagnose ondersteunen:</span><span class="sxs-lookup"><span data-stu-id="40b72-113">The following snippet will fail when executed on machines which support this diagnostic:</span></span>

```qsharp
within {
    AllowAtMostNQubits(3, "Too many qubits allocated.");
} apply {
    // Fails since this allocates four qubits.
    using (register = Qubit[4]) {
    }
}
```

## <a name="remarks"></a><span data-ttu-id="40b72-114">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="40b72-114">Remarks</span></span>

<span data-ttu-id="40b72-115">Deze bewerking kan worden vervangen door een van de doelen die deze niet ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="40b72-115">This operation may be replaced by a no-op on targets which do not support it.</span></span>