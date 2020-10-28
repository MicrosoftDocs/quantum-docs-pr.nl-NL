---
uid: Microsoft.Quantum.Diagnostics.AllowAtMostNQubits
title: Bewerking AllowAtMostNQubits
ms.date: 10/26/2020 12:00:00 AM
ms.topic: article
qsharp.kind: operation
qsharp.namespace: Microsoft.Quantum.Diagnostics
qsharp.name: AllowAtMostNQubits
qsharp.summary: Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.
ms.openlocfilehash: ddbed96df0d95cfd78730c091a6a81ee6e49c349
ms.sourcegitcommit: 29e0d88a30e4166fa580132124b0eb57e1f0e986
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/27/2020
ms.locfileid: "92702789"
---
# <a name="allowatmostnqubits-operation"></a><span data-ttu-id="d51d5-102">Bewerking AllowAtMostNQubits</span><span class="sxs-lookup"><span data-stu-id="d51d5-102">AllowAtMostNQubits operation</span></span>

<span data-ttu-id="d51d5-103">Naam ruimte: [micro soft. Quantum. Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span><span class="sxs-lookup"><span data-stu-id="d51d5-103">Namespace: [Microsoft.Quantum.Diagnostics](xref:Microsoft.Quantum.Diagnostics)</span></span>

<span data-ttu-id="d51d5-104">Pakket [](https://nuget.org/packages/)</span><span class="sxs-lookup"><span data-stu-id="d51d5-104">Package: [](https://nuget.org/packages/)</span></span>


<span data-ttu-id="d51d5-105">Tussen een aanroep van deze bewerking en de adjoint, wordt met behulp van-instructies gecontroleerd of er Maxi maal een gegeven aantal extra qubits is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="d51d5-105">Between a call to this operation and its adjoint, asserts that at most a given number of additional qubits are allocated with using statements.</span></span>

```qsharp
operation AllowAtMostNQubits (nQubits : Int, message : String) : Unit
```


## <a name="input"></a><span data-ttu-id="d51d5-106">Invoer</span><span class="sxs-lookup"><span data-stu-id="d51d5-106">Input</span></span>

### <a name="nqubits--int"></a><span data-ttu-id="d51d5-107">nQubits: [int](xref:microsoft.quantum.lang-ref.int)</span><span class="sxs-lookup"><span data-stu-id="d51d5-107">nQubits : [Int](xref:microsoft.quantum.lang-ref.int)</span></span>

<span data-ttu-id="d51d5-108">Het maximum aantal qubits dat kan worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="d51d5-108">The maximum number of qubits that may be allocated.</span></span>


### <a name="message--string"></a><span data-ttu-id="d51d5-109">bericht: [teken reeks](xref:microsoft.quantum.lang-ref.string)</span><span class="sxs-lookup"><span data-stu-id="d51d5-109">message : [String](xref:microsoft.quantum.lang-ref.string)</span></span>

<span data-ttu-id="d51d5-110">Een bericht dat wordt weer gegeven wanneer de fout is opgetreden.</span><span class="sxs-lookup"><span data-stu-id="d51d5-110">A message to be displayed upon failure.</span></span>



## <a name="output--unit"></a><span data-ttu-id="d51d5-111">Output: [eenheid](xref:microsoft.quantum.lang-ref.unit)</span><span class="sxs-lookup"><span data-stu-id="d51d5-111">Output : [Unit](xref:microsoft.quantum.lang-ref.unit)</span></span>



## <a name="remarks"></a><span data-ttu-id="d51d5-112">Opmerkingen</span><span class="sxs-lookup"><span data-stu-id="d51d5-112">Remarks</span></span>

<span data-ttu-id="d51d5-113">Deze bewerking kan worden vervangen door een van de doelen die deze niet ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="d51d5-113">This operation may be replaced by a no-op on targets which do not support it.</span></span>