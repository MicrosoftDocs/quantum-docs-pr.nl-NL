---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNQubits
title: Bewerking AllowAtMostNQubits
ms.date: 11/25/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNQubits
qsharp.summary: Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.
ms.openlocfilehash: 5376b6f39d12d664342fbf71e67442c6ef8a0827
ms.sourcegitcommit: a87c1aa8e7453360025e47ba614f25b02ea84ec3
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/26/2020
ms.locfileid: "96202546"
---
# <a name="allowatmostnqubits-operation"></a><span data-ttu-id="48f3c-102">Bewerking AllowAtMostNQubits</span><span class="sxs-lookup"><span data-stu-id="48f3c-102">AllowAtMostNQubits operation</span></span>

<span data-ttu-id="48f3c-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="48f3c-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="48f3c-104">Pakket: [micro soft. Quantum. Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span><span class="sxs-lookup"><span data-stu-id="48f3c-104">Package: [Microsoft.Quantum.Standard](https://nuget.org/packages/Microsoft.Quantum.Standard)</span></span>


<span data-ttu-id="48f3c-105">Tussen een aanroep van deze bewerking en de adjoint, wordt met behulp van-instructies gecontroleerd of er Maxi maal een gegeven aantal extra qubits is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="48f3c-105">Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.</span></span>

```qsharp
operation AllowAtMostNQubits (nQubits : Int, message : String) : Unit is Adj
```


## <a name="input"></a><span data-ttu-id="48f3c-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="48f3c-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="48f3c-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="48f3c-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="48f3c-108">Het maximum aantal qubits dat kan worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="48f3c-108">The maximum number of qubits that may be allocated.</span></span>


### <a name="message--string"></a><span data-ttu-id="48f3c-109">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="48f3c-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="48f3c-110">Een bericht dat wordt weer gegeven wanneer de fout is opgetreden.</span><span class="sxs-lookup"><span data-stu-id="48f3c-110">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="48f3c-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="48f3c-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="48f3c-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="48f3c-112">Remarks</span></span>

<span data-ttu-id="48f3c-113">Deze bewerking kan worden vervangen door een van de doelen die deze niet ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="48f3c-113">This operation may be replaced by a no-op on targets which do not support it.</span></span>